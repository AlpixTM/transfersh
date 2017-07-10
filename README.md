# transfersh
unofficial command-line client for https://github.com/dutchcoders/transfer.sh (https://transfer.sh)

### Usage

#### Upload file        
        transfersh filename
        >>>>File saved at: https://transfer.sh/XXXXX/filename
#### Upload file && change the name    
        transfersh -n new_filename filename
        >>>>File saved at: https://transfer.sh/XXXXX/new_filename
#### Upload all files in directory recursively
        transfersh  -r /xx/xy/
        File /xx/xy/TEST.txt saved at: https://transfer.sh/XXXXX/TEST.txt
        File /xx/xy/yy/testtest.txt saved at: https://transfer.sh/XXXXX/testtest.txt
#### Upload all files in current directory recursively && change the name
        transfersh  -r ./ -n test.txt
        File ./TEST.txt saved at: https://transfer.sh/XXXXX/test.txt
        File ./testtest.txt saved at: https://transfer.sh/XXXXX/test.txt
#### Upload all files as gzip compressed tar 
        transfersh -rtg ./ -n myupload-as-tar-gz.tar.gz
        File saved at: https://transfer.sh/XXXXX/myupload-as-tar-gz.tar.gz
#### Upload all files as uncompressed tar
        transfersh -rt ./ -n myupload-as-tar.tar
        File saved at: https://transfer.sh/XXXXX/myupload-as-tar.tar
#### Check file for virus with [Virustotal](https://www.virustotal.com)    
        transfersh -vt filename
        Virustotal Report is available here: https://www.virustotal.com/file/....
        
### Install
##### Debian / Ubuntu
(Tested on Debian & elementary OS & Ubuntu)

    1. echo "deb [trusted=yes] http://mirror.alpix.eu/ debianpkg/" >> /etc/apt/sources.list
    2. apt-get update && apt-get upgrade
    3. apt-get install transfersh -y
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
