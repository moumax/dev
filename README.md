# dev-env

Set-ExecutionPolicy AllSigned

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

choco install chocolateygui

// software to install :
choco install nvidia-display-driver vlc-nightly runjs firefox adobereader ocenaudio

choco install vscode

// To upgrade
choco upgrade all --except="'skype,conemu'"

// Install wsl
``
// In powershell admin mode :

wsl --list --online
wsl --install -d <Distribution Name>
``
