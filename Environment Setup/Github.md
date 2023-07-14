# Prerequisite

## Windows

[Git Bash](https://gitforwindows.org/)

# SSH Setup

Open Git Bash

`ssh-keygen -t ed25519 -C "your_github_email@example.com"`

When prompted to enter a name for your key you can either use the default one or create a key specific to this connection
You can also should to secure your ssh key with a passphrase

After Creating the key add it to the ssh-agent

`ssh-add ~/.ssh/id_ed25519`

Note: [Auto-launch ssh-agent on window](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases#auto-launching-ssh-agent-on-git-for-windows)

