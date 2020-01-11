# transfersh
unofficial command-line client for https://github.com/dutchcoders/transfer.sh (https://transfer.sh)

### Documentation
  * [Usage](#usage)
  * [Install](#install)

### Usage 
<a name="usage"></a>

#### Upload file        
        >transfersh file.txt
        File file.txt saved at: https://transfer.sh/XXXXX/file.txt
#### Upload file with progress bar       
        >transfersh -p file.txt
        Upload: [#####################################-----------] 75.68%
        File file.txt saved at: https://transfer.sh/XXXXX/file.txt
#### Upload file && change the name
        >transfersh -n newname.txt file.txt
        File file.txt saved at: https://transfer.sh/XXXXX/newname.txt
#### Upload to your transfersh server instead of https://transfer.sh
        >transfersh -sn upload.server.name filename
        File saved at: https://upload.server.name/XXXXX/filename
#### Upload all files in directory recursively
        >transfersh  -r /xx/xy/
        File /xx/xy/TEST.txt saved at: https://transfer.sh/XXXXX/TEST.txt
        File /xx/xy/yy/testtest.txt saved at: https://transfer.sh/XXXXX/testtest.txt
#### Upload all files in current directory recursively && change the name
        >transfersh  -r ./ -n test.txt
        File ./TEST.txt saved at: https://transfer.sh/XXXXX/test.txt
        File ./testtest.txt saved at: https://transfer.sh/XXXXX/test.txt
#### Upload all files as gzip compressed tar 
        >transfersh -rtg ./ -n myupload-as-tar-gz.tar.gz
        File saved at: https://transfer.sh/XXXXX/myupload-as-tar-gz.tar.gz
#### Upload all files as uncompressed tar
        >transfersh -rt ./ -n myupload-as-tar.tar
        File saved at: https://transfer.sh/XXXXX/myupload-as-tar.tar
#### Upload all files as zip
        >transfersh -rz ./ -n myupload-as-zip.zip
        File saved at: https://transfer.sh/XXXXX/myupload-as-zip.zip
#### Save all URLs in textfile
        >transfersh -r ./ -s URLS.txt
        File ./TEST.txt saved at: https://transfer.sh/XXXXX/test.txt
        File ./testtest.txt saved at: https://transfer.sh/XXXXX/test.txt
#### Save all URLs in textfile and upload it
        >transfersh -r ./ -s URLS.txt
        File ./TEST.txt saved at: https://transfer.sh/XXXXX/test.txt
        File ./testtest.txt saved at: https://transfer.sh/XXXXX/test.txt
        File /tmp/transfersh-savefile.txt saved at: https://transfer.sh/XXXXX/transfersh-savefile.txt
#### Check file for virus with [Virustotal](https://www.virustotal.com)    
        >transfersh -vt filename
        Virustotal Report is available here: https://www.virustotal.com/file/....



### Install 
<a name="install"></a>
##### Debian / Ubuntu
    (Out of date at the moment!)
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
