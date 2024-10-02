# 42_vm
Recreate the workspace of the 42 in a vm

Some useful tips to create a virtual machine with all the tools you need to work on projects of the 42 school wherever you want.

## Summary

* [Virtualization](#virtualization)
* [Operating System](#operating-system)
* [Tools](#tools)


## Virtualization

- Oracle VM VirtualBox : https://www.virtualbox.org

## Operating System

- Ubuntu LTS : https://ubuntu.com
- Xubuntu LTS : https://xubuntu.org
- Lubuntu LTS : https://lubuntu.me

choose xubuntu for a fair compromise between performance and features.

Fell free to use this [banner](./vm_description.txt) to remember the username and password chosen.

## Tools

- Install Vim:
```
sudo apt-get install vim
```
- Install git:
```
sudo apt-get install git
```
- Install curl:
```
sudo apt-get install curl
```
- Install Zsh and set as default login shell for the current user:
```
sudo apt-get install zsh
sudo usermod -s $(which zsh) $(whoami)
```
- Run zsh and press the number key 2 and ZSH should create a new ~/.zshrc configuration file with the recommended settings, then reboot the system.

- Customize Zsh with [Oh My Zsh](https://ohmyz.sh):

  `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

  **NOTE: the installer will rename an existing `.zshrc` file to `.zshrc.pre-oh-my-zsh`.**
  
 - It is possible to customize Zsh more thoroughly:
    - Set [agnoster](https://github.com/agnoster/agnoster-zsh-theme) as a default theme:
    
      `sed -i 's/ZSH_THEME=".*"/ZSH_THEME="agnoster"/' ~/.zshrc`
      
      **NOTE: In all likelihood, you will need to install a Powerline-patched font for this theme to render correctly:**
      
      `sudo apt-get install fonts-powerline`
      
     - Download and configure [Dracula Theme](https://draculatheme.com/xfce4-terminal):
     
        After put the file in the specified folder:
        
        Open "Xfce Terminal Settings" --> "Colors" --> "Load Presets.." --> Select Dracula
        
     - Download and configure [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md#oh-my-zsh)
     - Download and configure [zsh-syntax-higlighting](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md#oh-my-zsh)

- Install the VirtualBox Guest Additions:
  ```
  sudo apt update
  sudo apt install build-essential dkms linux-headers-$(uname -r)
  ```
  Mount the Guest Additions CD Image e run the script for Linux, then reboot

- Install gcc:
  ```
  sudo apt-get install gcc
  ```
- Some Info of the gcc configuration of the Mac on the cluster:

  - **Mac with MacOS:**
    
    - [Output](./gcc_define_cluster_macos.txt) of:
      
      ```
      gcc -dM -E - </dev/null > gcc_define_cluster_macos.txt
      ```
    - [Output](./gcc_version_macos.txt) of:
      
      ```
      gcc -v 2> gcc_version_macos.txt
      ```

  - **Mac with Ubuntu LTS:**
    
    - [Output](./gcc_define_cluster_ubuntu.txt) of:
      
      ```
      gcc -dM -E - </dev/null > gcc_define_cluster_ubuntu.txt
      ```
    - [Output](./gcc_version_ubuntu.txt) of:
      
      ```
      gcc -v 2> gcc_version_ubuntu.txt
      ```
      
## 42 Tools

- **Install Norminette:**
  
  Follow the instruction of the official github repository [here](https://github.com/42School/norminette)

- **Install the 42 standard header for vim editor:**
  
  Follow the instruction of the official github repository [here](https://github.com/42Paris/42header)
  
