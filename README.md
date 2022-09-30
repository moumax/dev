# Installation for dev web environment on windows 10/11

## Install chocolatey

- To find a package
  - <https://community.chocolatey.org/packages>

````powershell
    Set-ExecutionPolicy AllSigned
    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
    choco install flow-launcher gimp ocenaudio transmission vscode insomnia-rest-api-client firefox runjs vlc adobereader dbeaver discord nvidia-display-driver
````

- To upgrade softwares

````powershell
    choco upgrade all --except="'skype,conemu'"
````

## Install wsl

- In powershell admin mode
  
  ````powershell
    wsl --list --online
    wsl --install -d <distribution name>
  ````

## Install zsh

````bash
sudo apt install zsh
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
    source ~/.zshrc
    nvm ls-remote
    nvm install vXX.XX
    nvm use vXX.XX
````

## Install mysql

````bash
    sudo apt install mysql-server
    sudo service mysql start
    sudo mysql
    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by 'XXXXXX';
    sudo mysql_secure_installation
    mysql -u root -p
    CREATE USER 'XXXXXX'@'localhost' IDENTIFIED BY 'XXXXXX';
    GRANT ALL PRIVILEGES ON *.* TO 'XXXXXX'@'localhost';
````

## Install git ssh key

````bash
ssh-keygen -t ed25519 -C "XXXXX.XXXXX@gmail.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
````

- Add the ssh key to github
  
  - https://github.com/settings/keys

- Add the git config in shell
  
````bash
    git config --global user.name "XXX XXXXX"
    git config --global user.email "XXXX.XXXXX@gmail.com"
````

## Retreive configuration in vscode

## Change keyboard speed on windows