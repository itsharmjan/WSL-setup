# WSL-setup
This playbook will setup my WSL2

Requirements:
- git
- python3
- ansible



How to run:

ansible-playbook playbook_install_ohmyzsh.yaml -K

ansible-playbook playbook_setup_wsl.yaml -K --vault-id homelab@~/.vaults/homelab.vault