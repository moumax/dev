# dev-env

``
Set-ExecutionPolicy AllSigned
``

``
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

``

``
choco update chocolatey
``

``
choco install nvidia-display-driver vlc-nightly runjs firefox adobereader ocenaudio
choco install vscode
``

``
choco upgrade all --except="'skype,conemu'"
``

``
wsl --list --online
wsl --install -d <Distribution Name>
``
