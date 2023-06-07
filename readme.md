## What is TorGhost ?
TorGhost is an anonymization script. TorGhost redirects all internet traffic through SOCKS5 tor proxy. DNS requests are also redirected via tor, thus preventing DNSLeak. The scripts also disables unsafe packets exiting the system. Some packets like ping request can compromise your identity.

## Build and install from source (Updated for Python v3.11)
`git clone https://github.com/SusmithKrishnan/torghost.git`

`cd torghost`

`chmod +x build.sh`

`./build.sh`

### Fix for "torghost.c:6:10: fatal error: Python.h: No such file or directory"
Simply go inside 'build.sh' file and edit the 
"gcc -Os -I /usr/include/python3.8 -o torghost torghost.c -lpython3.8 -lpthread -lm -lutil -ldl" 
to
"gcc -Os -I /usr/include/python[YOUR-PYTHON-VERSION] -o torghost torghost.c -lpython[YOUR-PYTHON-VERSION] -lpthread -lm -lutil -ldl"
It will now build and compile. Cheers!

## How to install ?
**New kali update is causing permission error, please build and install from source**

~~TorGhost can be installed by downloading the [latest release](https://github.com/SusmithKrishnan/torghost/releases) using debian package manager~~

~~Download~~

~~` wget -c https://github.com/SusmithKrishnan/torghost/releases/download/v3.0.2/torghost-3.0.2-amd64.deb`~~

~~In the downloaded folder use dpkg to install~~

~~`sudo dpkg -i torghost-*-amd64.deb`~~


#### Alternate method (support for previous install script)
The *install.sh* script also does the same. Its for users following old tutorials.

`git clone https://github.com/SusmithKrishnan/torghost.git`

`cd torghost`

`chmod +x install.sh`

`./install.sh`


## Usage
Torghost v3.0 usage:

`  -s      --start        Start Torghost`

`  -r      --switch       Request new tor exit node`

`  -x      --stop         Stop Torghost`

`  -h      --help         Print this help and exit`

`  -u      --update       Checks for updates`





