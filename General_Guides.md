
 
 


# General Guides and Commands for noobs 
## Reminders because I have  the memory of a goldfish


 :pushpin:  If you forget to run SUDO on a command you can run ```SUDO !!``` it will rerun the last command as sudo


```shell
# Move data to Linux using  SCP 
   scp [OPTION] [user@]SRC_HOST:]file1 [user@]DEST_HOST:]file2

   scp file.txt remote_username@10.10.0.2:/remote/directory 

```
```shell
# Move data to Linux using  sftp
  sftp username@servername or ip 
  lls [gets local dir contents]
  ls  [gets remote file contnets]
  lcd  [ you get the idea]
  cd  

  put  filename  [ place a file on the remote server ]
  get  filename  [ pulls files  down to local system ]

```
# Getting Started with SSH key pair
```shell
ssh-keygen -t ed25519 -C "your_email@example.com" 
```
-  Add public and private key to password manager
- place the  private key in your .ssh folder
  -  windows   it will be your ```username/.ssh ~/.ssh``` should work as well  you will need to show hidden files
  -  linux its your home directory  ```~/.ssh```  ``` ls -a ``` will show all files in your homedir
- Make sure  your user is the only one that can access  this  directory
-  you may place the public key on a any system that you wish to access byt adding it to the ``` authorized_keys``` file  you may have to create this file ```touch authorized_keys``` and all the public keys that you wisht  to have access to the system  sudo wil still require a password
```bash 
#deploy key to remote host 
ssh-copy-id  -i key.pub username@xx.xx.xx.xx
```



  # Expand ubuntu lv volume  and partition 

```shell
       cfdisk
       vgdisplay
       lvdisplay 

         cfdisk 
         -
         sudo parted /dev/sda
         resizepart 3
         sudo pvresize /dev/sda3
         sudo lvextend -l +100%FREE /dev/ubuntu-vg/ubuntu-lv
         sudo resize2fs /dev/ubuntu-vg/ubuntu-lv
```         

> CheatSheet
>> https://ostechnix.com/tmux-command-examples-to-manage-multiple-terminal-sessions/