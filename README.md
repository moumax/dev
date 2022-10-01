# Installation for dev web environment on windows 10/11

## Install chocolatey

- To find a package
  - <https://community.chocolatey.org/packages>

````powershell
    Set-ExecutionPolicy AllSigned
    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
    choco install flow-launcher gimp ocenaudio transmission vscode insomnia-rest-api-client firefox runjs vlc adobereader dbeaver discord nvidia-display-driver bitwarden-chrome
````

- To upgrade softwares

````powershell
    choco upgrade all --except="'skype,conemu'"
````

## Install wsl

- In powershell admin mode
  
  ````powershell
    wsl --list --online
  ````

  ````powershell
    wsl --install -d <distribution name>
  ````

## Install zsh

````bash
sudo apt install zsh
````

````bash
chsh -s $(which zsh)
````

- Install Ohmyzsh
  
````bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
````

## Replace .bashrc or .zshrc on distro

## Replace the terminal configuration file

## Install nvm

````bash
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | zsh
````

````bash
    source ~/.zshrc
````

````bash
    nvm ls-remote
````

````bash
    nvm install vXX.XX
````

````bash
    nvm use vXX.XX
````

## Install mysql

````bash
    sudo apt install mysql-server
````

````bash
    sudo service mysql start
````

````bash
    sudo mysql
````

````bash
    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'XXXXXX';
````

````bash
    sudo mysql_secure_installation
````

````bash
    mysql -u root -p
````

````bash
    CREATE USER 'XXXXXX'@'localhost' IDENTIFIED BY 'XXXXXX';
````

````bash
    GRANT ALL PRIVILEGES ON *.* TO 'XXXXXX'@'localhost';
````

## Install git ssh key

````bash
ssh-keygen -t ed25519 -C "XXXXX.XXXXX@gmail.com"
````

````bash
eval "$(ssh-agent -s)"
````

````bash
ssh-add ~/.ssh/id_ed25519
````

````bash
cat ~/.ssh/id_ed25519.pub
````

- Add the ssh key to github
  
  - https://github.com/settings/keys

- Add the git config in shell
  
````bash
    git config --global user.name "XXX XXXXX"
````

````bash
    git config --global user.email "XXXX.XXXXX@gmail.com"
````

## Retreive configuration in vscode

## Change keyboard speed on windows
