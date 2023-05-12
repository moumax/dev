# dev-env

## POWERSHELL
```
Set-ExecutionPolicy AllSigned
```
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
## CHOCO
```
choco update chocolatey
```

```
choco install nvidia-display-driver vlc-nightly runjs firefox adobereader ocenaudio powertoys dbeaver vscode
```

```
choco upgrade all --except="'skype,conemu'"
```

## WSL

```
wsl --list --online
wsl --install -d <Distribution Name>
```

## FONT WINDOWS TERMINAL
[Anonymous Pro](https://www.marksimonson.com/fonts/view/anonymous-pro)
wsl by default
change font on terminal preview
change transparency 70%

## ZSH
```
sudo apt install zsh
chsh -s $(which zsh)
exit
q
```

## OHMYZSH

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
### CHANGE .ZSHRC
```
ZSH_THEME="gnzh"

plugins=(
    git
    zsh-autosuggestions
    zsh-syntax-highlighting
)
```
```
source .zshrc
```

## NVM
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | zsh
source ~/.zshrc
nvm install --lts
```

## GIT
```
ssh-keygen -t ed25519 -C "marc.lantol@gmail.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```

### GIT CONFIG
```
git config --global user.name "Marc LANTOL"
git config --global user.email "marc.lantol@gmail.com"
git config --global init.defaultBranch main
```

### ADD GIT KEY
[github](https://github.com/settings/keys)

## MYSQL
```
sudo apt install mysql-server
sudo update-rc.d mysql defaults
sudo mysql
```
```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by '********';
exit
```
```
sudo mysql_secure_installation
```
```
mysql -h 127.0.0.1 -P 3306 -u root -p
```
```
CREATE USER 'marco'@'localhost' IDENTIFIED BY '******';
```
```
GRANT ALL PRIVILEGES ON *.* TO 'marco'@'localhost';
```
```
exit
```

## SPEEDUP KEYBOARD
HKEY_CURRENT_USER\Control Panel\Accessibility\Keyboard Response

AutoRepeatDelay = 200
AutoRepeatRate = 9
DelayBeforeAcceptance = 0
Flags = 59

