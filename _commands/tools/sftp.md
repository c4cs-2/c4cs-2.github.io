# sftp
sftp stands for SSH File Transfer Protocol (or Secure File Transfer Protocol) and is a network protocol that allows users to securely transfer files from remote servers over a network connection. sftp operates over the SSH protocol and is an encrypted form of ftp.

## Useful Options / Examples

### Open interactive session
this logs you into the remote system (after prompting you for your password) and allows you to interact with a sftp prompt (similar to the command prompt on your local machine) 

    $ sftp user@hostname
      user@hostname's password:
      Connected to hostname.
    sftp>

### Retrieve file (without Interactive Session)
this allows you to log into the remote system (after prompting you for your password) and automatically retrieve files whose path is specified in the command and exit 

    $ sftp user@hostname:documents/example.zip
      user@hostname's password:
      Fetching /home/myname/documents/example.zip to example.zip

you can also specify the location where you want to download the file

    $ sftp user@hostname:documents/example.zip /downloads

you can even rename the file you just retrieved

    $ sftp user@hostname:documents/example.zip /downloads/new_example.zip


### Retrieving multiple files with wildcard character (*)
this allows you to specify wildcards in the filename for files to retrieve

    $ sftp user@hostname:documents/*.zip

this would retrieve all the files in the /documents directory that has the .zip extension
  
### Some standard SFTP commands

these commands all operate in **the interactive mode** on **the remote host** 

Command | Function
------------ | -------------
**bye** | close the session and exit sftp
**chmod** mode path | change permissions of path file
**chown** user path | change owner of path file
**exit** | close the session and exit sftp
**get** [-Ppr] remote_path [local_path] | retrieve remote_path from remote host and download it to local_path on local machine; -P and -p flags (if used) copies permissions and access times; -r flag (if used) copies directories recursively
**help** | get a help message that lists the sftp commands
**cd** path | change working directory to path
**ls** | list files in current directory
**mkdir** path | create a new directory 
**put** [-Ppr] local_path [remote_path] | upload local_path to remote_path on the remote machine; -P and -p flags (if used) copies permissions and access times; -r flag (if used) copies directories recursively
**pwd** | print working directory
**rename** old_path new_path | rename old_path to new_path
**rm** path | delete the file 
**rmdir** path | delete the directory
**version** | display version of sftp protocol
**!** | pop into local shell and type **exit** to return to sftp shell
**?** | get a help message that lists the sftp commands









