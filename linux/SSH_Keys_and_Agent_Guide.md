
# Managing SSH Keys and SSH Agent on WSL and Windows

This guide covers the process of creating an SSH key with Windows Subsystem for Linux (WSL), adding the key to a server for SSH access, and managing the SSH agent on both WSL and Windows.

## Creating the SSH Key via WSL

1. Open your WSL terminal.

2. Generate a new SSH key pair by running:

	```bash
	ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
	```

	Replace `"your_email@example.com"` with your actual email or a meaningful comment.

3. When prompted to "Enter a file in which to save the key," press Enter to use the default location, or specify a path where you want to save the key.

4. Enter a passphrase for added security when prompted, or press Enter to leave it empty (not recommended).

## Adding the SSH Key to the Server

1. Display your public key with:

	```bash
	cat ~/.ssh/id_rsa.pub
	```

	Adjust the path if you saved your key pair in a non-default location.

2. Copy the output of the command.

3. Log into your server with SSH.

4. Edit the `~/.ssh/authorized_keys` file:

	```bash
	nano ~/.ssh/authorized_keys
	```

5. Paste your public key into this file on a new line. Save and close the file.

## Managing SSH Agent on WSL

### Starting the SSH Agent

1. Start the SSH agent in the background:

   ```bash
   eval $(ssh-agent -s)
   ```

2. Add your SSH private key to the agent:

   ```bash
   ssh-add ~/.ssh/id_rsa
   ```

   Replace the path with the location of your private key if different.

### Adding Keys Automatically (Optional)

To automatically add your keys when you open a new terminal session, add the following to your `~/.bashrc` or `~/.zshrc` file:

```bash
if [ -z "$SSH_AUTH_SOCK" ] ; then
	eval $(ssh-agent -s)
	ssh-add ~/.ssh/id_rsa
fi
```

or make a script

```bash
echo '#!/bin/bash' > ssh-add-keys.sh
echo 'eval $(ssh-agent -s)' >> ssh-add-keys.sh
echo 'ssh-add ~/.ssh/id_rsa_paco' >> ssh-add-keys.sh
echo 'ssh-add ~/.ssh/id_rsa_root' >> ssh-add-keys.sh
chmod +x ssh-add-keys.sh
```

## Managing SSH Agent on Windows via PowerShell

### Enabling the SSH Agent Service

1. Open PowerShell as Administrator.

2. Enable and start the SSH Agent service:

   ```powershell
   Set-Service ssh-agent -StartupType Automatic
   Start-Service ssh-agent
   ```

### Adding Your SSH Key to the Agent

1. Add your private key to the SSH agent:

	```powershell
	ssh-add C:\path\to\your\private\key
	```

	Replace `C:\path\to\your\private\key` with the Windows path to your private key file.

---

Save these instructions in a `.md` file for easy reference. This guide provides a straightforward approach to managing SSH keys and the SSH agent across WSL and Windows, ensuring secure and convenient SSH access.
