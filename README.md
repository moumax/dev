# dev-env

## TERMINAL PREVIEW
Change powershell to run on admin on only

## POWERSHELL
```powershell
Set-ExecutionPolicy AllSigned
```
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
___
## CHOCO

### Laptop
```powershell
choco install vlc runjs dbeaver adobereader ocenaudio powertoys vscode
```

### Desktop
```powershell
choco install nvidia-display-driver vlc runjs adobereader ocenaudio dbeaver vscode msiafterburner steam git obsidian
```

### Update
```powershell
choco upgrade all --except="'skype,conemu'"
```
___
## WSL

```powershell
wsl --list --online
```
```powershell
wsl --install -d <Distribution Name>
```
___
## FONT WINDOWS TERMINAL
[jetbrains mono](https://www.jetbrains.com/fr-fr/lp/mono/)
wsl by default
change font on terminal preview
change transparency 70%
___
## ZSH
```bash
sudo apt install zsh
chsh -s $(which zsh)
exit
q
```
___
## OHMYZSH

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
### CHANGE .ZSHRC
```bash
ZSH_THEME="gnzh"

plugins=(
    git
    zsh-autosuggestions
    zsh-syntax-highlighting
)
```
```bash
source .zshrc
```
___
## NVM
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | zsh
source ~/.zshrc
nvm install --lts
```
___
## GIT
```bash
ssh-keygen -t ed25519 -C "marc.lantol@gmail.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```

### GIT CONFIG
```bash
git config --global user.name "Marc LANTOL"
git config --global user.email "marc.lantol@gmail.com"
git config --global init.defaultBranch main
```

### ADD GIT KEY
[github key](https://github.com/settings/keys)
___
## MYSQL
```bash
sudo apt install mysql-server
sudo update-rc.d mysql defaults
sudo mysql
```
```sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password by '********';
exit
```
```bash
sudo mysql_secure_installation
```
```sql
mysql -h 127.0.0.1 -P 3306 -u root -p
```
```sql
CREATE USER 'marco'@'localhost' IDENTIFIED BY '******';
```
```sql
GRANT ALL PRIVILEGES ON *.* TO 'marco'@'localhost';
```
```sql
exit
```
___

## SPEEDUP KEYBOARD
HKEY_CURRENT_USER\Control Panel\Accessibility\Keyboard Response
```
AutoRepeatDelay = 200
AutoRepeatRate = 9
DelayBeforeAcceptance = 0
Flags = 59
```
___

## VSCODE
Retreive github config
Install extensions also on wsl

## NVIM
```bash
sudo apt install build-essential software-properties-common -y
sudo add-apt-repository ppa:neovim-ppa/unstable -y
sudo apt-get update
sudo apt install neovim -y
```
### RIPGREP
```
sudo apt-get install ripgrep
```
### NVCHAD
https://nvchad.com/

