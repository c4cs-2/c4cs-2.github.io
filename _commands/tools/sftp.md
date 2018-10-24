# sftp
sftp stands for SSH File Transfer Protocol (or Secure File Transfer Protocol) and is a network protocol that allows users to securely transfer files from remote servers over a network connection. SFTP operates over the SSH protocol and is an encrypted form of ftp.

## Useful Options / Examples

### Open Interactive Session
this logs you into the remote system (after prompting you for your password) and allows you to interact with a sftp prompt (similar to the command prompt on your local machine) 

 $ sftp user@hostname
   user@hostname's password:
 Connected to hostname.
 sftp>

### Retrieve files (without Interactive Session)
this allows you to log into the remote system (after prompting you for your password) and automatically retrieves files specified in the command


