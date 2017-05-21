# transfersh
unofficial command-line client for https://github.com/dutchcoders/transfer.sh (https://transfer.sh)

### Usage
        transfersh filename

### Install
##### Debian / Ubuntu
(Tested on Debian & elementary OS & Ubuntu)

    1. echo "deb http://mirror.alpix.eu/ debianpkg/" >> /etc/apt/sources.list
    2. apt-get update && apt-get upgrade
    3. apt-get install transfersh -y --force-yes
#### Arch-based systems

        If you can access the AUR with your package manager (https://aur.archlinux.org/):
            e.g. yaourt as package manager:  
                1.  yaourt -S transfersh
        If not do it manually
            1. curl -L -O https://aur.archlinux.org/cgit/aur.git/snapshot/transfersh.tar.gz
            2. tar xf transfersh.tar.gz
            3. cd transfersh && makepkg -si
        *Last step: Vote on aur if the package is useful for you. <3*
#### PLEASE FEEL FREE TO CONTRIBUTE!
Just create a Pull request...
