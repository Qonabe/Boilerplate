# Github

## Prerequisite

### Windows

[Git Bash](https://gitforwindows.org/)
[Github CLI](https://cli.github.com/)

Configure
Git Bash: `export PATH=$PATH:PATH_TO_GITHUB_CLI_INSTALL_DIRECTORY`

PATH_TO_GITHUB_CLI_INSTALL_DIRECTORY is the folder containing the gh.exe (if you're on windows) is. It should be in the form `/c/foo/bar/baz/Github\ CLI/`.
Note the backslash before the space. Of course this comment is valid only if your path DOES have a space in it.

Git Bash: `gh auth login`

## SSH Setup

Open Git Bash

`ssh-keygen -t ed25519 -C "your_github_email@example.com"`

When prompted to enter a name for your key you can either use the default one or create a key specific to this connection
You can also should to secure your ssh key with a passphrase

After Creating the key add it to the ssh-agent

`ssh-add ~/.ssh/id_ed25519`

Note: [Auto-launch ssh-agent on window](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases#auto-launching-ssh-agent-on-git-for-windows)

## Uses

### Creating an empty repo on github and cloning it

Github CLI: `gh repo create PROJECT_NAME --public|private|internal --clone`

(if creating a project belonging to an organization use the 'organization-name/project-name' pattenr for the name)
For the full list of arguments see the [Github CLI Manual](https://cli.github.com/manual/gh_repo_create)

### Creating a new project and pushing it on github in a new repo

Create a project (see the Project Creation instructions corresponding to the type of project you want)

```
git init -b main
git add .
git commit -m "First commit"
```

Github CLI: `gh repo create PROJECT_NAME --source=PROJECT_PATH --public|private|internal --push`

(if creating a project belonging to an organization use the 'organization-name/project-name' pattenr for the name)
For the full list of arguments see the [Github CLI Manual](https://cli.github.com/manual/gh_repo_create)

