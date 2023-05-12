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
choco install nvidia-display-driver vlc-nightly runjs firefox adobereader ocenaudio powertoys dbeaver
choco install vscode
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


