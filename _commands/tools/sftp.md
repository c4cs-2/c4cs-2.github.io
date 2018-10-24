# sftp
sftp stands for SSH File Transfer Protocol (or Secure File Transfer Protocol) and is a network protocol that allows users to securely transfer files from remote servers over a network connection. SFTP operates over the SSH protocol and is an encrypted form of ftp.

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

    $  sftp user@hostname:documents/example.zip /downloads

you can even rename the file you just retrieved

    $ sftp user@hostname:documents/example.zip /downloads/new_example.zip


### Retrieving multiple files with wildcard 
this allows you to specify wildcards in the filename for files to retrieve

    $ sftp user@hostname:documents/*.zip

this would retrieve all the files in the /documents directory that has the .zip extension
  
### Some standard SFTP commands









