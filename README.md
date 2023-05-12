# dev-env

Set-ExecutionPolicy AllSigned

Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

choco install chocolateygui

// software to install :
nvidia-display-driver
brave
transmission
mysql workbench
postman
vlc-nightly
runjs
firefox
adobereader
ferdium
vscode
ocenaudio
intellijidea-ultimate

gimp

// To upgrade
choco upgrade all --except="'skype,conemu'"
