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

- Install gcc:
```
sudo apt-get install gcc
```
- Some Info of the gcc configuration of the Mac on the cluster:
  - [Output](./gcc_define_cluster.txt) of:
  ```
  gcc -dM -E - </dev/null > gcc_define_cluster.txt
  ```
  - Output of "gcc -v":
  ```
  Configured with: --prefix=/Applications/Xcode.app/Contents/Developer/usr --with-gxx-include-dir=/Library/Developer/CommandLineTools/SDKs/MacOSX.sdk/usr/include/c++/4.2.1
  Apple clang version 11.0.0 (clang-1100.0.33.17)
  Target: x86_64-apple-darwin18.7.0
  Thread model: posix
  InstalledDir: /Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin
``` 
