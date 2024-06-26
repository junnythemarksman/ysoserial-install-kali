# Introduction
Installing wine on Kali Linux is not advisable as it might pose a security risk. However, it is convenient when playing CTFs.


## To ensure that ysoserial.net gets installed in Kali Linux properly, follow these steps:
1) Install the following packages: `(sudo) apt install mono-complete wine winetricks -y`.
2) Then add `(sudo) dpkg --add-architecture i386`.
3) Update/upgrade using `(sudo) apt update && sudo apt upgrade -y`.
4) Install the 32-bit version using `(sudo) apt-get install wine32:i386`.
5) Add a new wine prefix using `WINEPREFIX="$HOME/.wine32" WINEARCH=win32 wine wineboot`. There's NO need to delete the 64-bit version on `~/.wine`.
6) Install dotnet using `winetricks dotnet48`. This will install it for both 64-bit and 32-bit versions and may take a while.
7) Get a copy of ysoserial.net at `https://github.com/pwntester/ysoserial.net/releases` or build your own by cloning the git repository.
8) Try to run any ysoserial.exe command `e.g. wine ysoserial.exe -f BinaryFormatter -g TypeConfuseDelegate -o base64 -c "ping 127.0.0.1"`.

## Reference
ysoserial.net repository: https://github.com/pwntester/ysoserial.net
