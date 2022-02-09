# 42_vm
Recreate the workspace of the 42 in a vm

Some useful tips to create a virtual machine with all the tools you need to work on projects of the 42 school wherever you want.

## Virtualization

- Oracle VM VirtualBox : https://www.virtualbox.org

## Operating System

- Ubuntu LTS : https://ubuntu.com
- Xubuntu LTS : https://xubuntu.org
- Lubuntu LTS : https://lubuntu.me

choose xubuntu for a fair compromise between performance and features.

## Tools

- Install Vim:
```
sudo apt-get install vim
```
- Install Zsh and set as default login shell for the current user:
```
sudo apt-get install zsh
sudo usermod -s $(which zsh) $(whoami)
```
- Run zsh and press the number key 2 and ZSH should create a new ~/.zshrc configuration file with the recommended settings, then reboot the system.

- Customize zsh :
```
sudo apt-get install zsh-autosuggestions
sudo apt-get install zsh-syntax-highlighting
```
