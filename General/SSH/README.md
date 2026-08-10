SSH (Secure Shell) is a cryptographic network protocol for securely operating network services -- most commonly remote login and file transfer -- over an unsecured network. If you deploy to servers, push to Git remotes, or transfer files, you use SSH.

- SSH
  - What is SSH and why it exists (replacing Telnet, FTP, rlogin)
  - Client / Server model
    - `sshd` (daemon) on the server
    - `ssh` client
  - Authentication methods 🔴
    - Password
    - Public-key (key pair) -- recommended
    - Two-factor (2FA)
  - SSH key pairs 🔴
    - Generate keys: `ssh-keygen -t ed25519 -C "email"`
    - Key types (RSA, ECDSA, **Ed25519** recommended)
    - Private key (`id_ed25519`) -- never share
    - Public key (`id_ed25519.pub`) -- share freely
    - Passphrase protection
  - Authorizing a key on a server
    - `ssh-copy-id user@host`
    - Manually adding to `~/.ssh/authorized_keys`
  - Connecting
    - `ssh user@host`
    - `ssh -p 2222 user@host` (custom port)
    - `-i` to specify a key file
  - SSH config file (`~/.ssh/config`)
    - Aliases for hosts 🔴
    - ```
      Host myserver
          HostName 192.168.1.10
          User deploy
          IdentityFile ~/.ssh/deploy_key
          Port 2222
      ```
  - Secure copy and file transfer
    - `scp local.txt user@host:/path/`
    - `sftp`
    - `rsync` over SSH (efficient sync)
  - Port forwarding (tunneling) 🔴
    - Local (`-L`)
    - Remote (`-R`)
    - Dynamic (`-D`, SOCKS proxy)
  - SSH agent
    - `eval "$(ssh-agent -s)"`
    - `ssh-add`
    - Agent forwarding (`-A`) -- and its security caveats
  - Server-side hardening 🔴
    - Disable password login (`PasswordAuthentication no`)
    - Disable root login (`PermitRootLogin no`)
    - Change default port (22)
    - Fail2ban
  - `known_hosts` and host key verification
  - Common errors
    - "REMOTE HOST IDENTIFICATION HAS CHANGED"
    - Permission denied (publickey)
    - Wrong file permissions on keys (`chmod 600`)
  - SSH and Git 🔴
    - GitHub/GitLab deploy keys
    - SSH URLs (`git@gitlab.com:...`)

---
🔴 Very Important
