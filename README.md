# WSL-setup
This playbook will setup my WSL2

Requirements:
- git
- python3
- ansible


# Install WSL
```shell
#install WSL
wsl --install Ubuntu
```

# Install font and update appearance
https://github.com/microsoft/cascadia-code 

# Prepare WSL to install playbooks
```shell
# update everything
sudo apt -y update
sudo apt -y upgrade

# install minimal required packages
sudo apt -y install python3-pip python3-venv unzip

# install homebrew and activate it for the current shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
brew completions link

# install ansible
brew install ansible
```

# Download this repo

# Run playbooks
```shell
ansible-playbook playbook_install_ohmyzsh.yaml -K

ansible-playbook playbook_setup_wsl.yaml -K --vault-id homelab@~/.vaults/homelab.vault
```