# Installation

## Install i3
[i3-man](https://i3wm.org/docs/repositories.html)

## Install kitty
```bash
sudo apt install kitty
```
## Install google chrome
[google-chrome-stable](https://doc.ubuntu-fr.org/google_chrome)

## Install neovim
```bash
sudo apt install software-properties-common -y
sudo add-apt-repository ppa:neovim-ppa/unstable -y
sudo apt-get update
sudo apt install neovim -y
```

## Modify bar on i3
```bash
/etc/i3status.conf
```

## Change battery display
[i3-man](https://faq.i3wm.org/question/6140/wrong-battery-percentage-shown-in-status-bar.1.html)

## Change brightness
[to-try](https://unix.stackexchange.com/questions/526653/control-screen-brightness-in-i3)

## Git
```bash
sudo apt install git
```
## Zsh
```bash
sudo apt install zsh
chsh -s $(which zsh)
```
## curl
```bash
sudo apt install curl
```

## Ohmyzsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

// git clone some plugins
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions


ZSH_THEME="gnzh"

plugins=(
    git
    zsh-autosuggestions
    zsh-syntax-highlighting
)
```

## Nvchad
```bash
sudo apt-get install ripgrep
sudo apt install build-essential
```

## Nvm
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | zsh
source ~/.zshrc

export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm-sh

nvm install --lts
```