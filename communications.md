

While working on a Linux operating system, you may need to communicate with other devices. For this, there are some basic utilities that you can make use of.
hese utilities can help you communicate with networks,other Linux systems and remote users.

SSH
SSH which stands for Secure Shell, It is used to connect to a remote computer securely. Compare to Telnet, SSH is secure wherein the client /server connection is authenticated using a digital certificate and passwords are encrypted. Hence it’s widely used by system administrators to control remote Linux servers.

SSH username@ip-address or hostname


### Ping
This utility is commonly used to check whether your connection to the server is healthy or not.This command is also used in –

Analyzing network and host connections
Tracking network performance and managing it
Testing hardware and software issues

ping 172.16.170.1

ping google.com


### FTP
FTP is file transfer protocol. It’s the most preferred protocol for data transfer amongst computers.

You can use FTP to –

- Logging in and establishing a connection with a remote host
- Upload and download files
- Navigating through directories
- Browsing contents of the directories


### Telnet
Telnet helps to –

- connect to a remote Linux computer
- run programs remotely and conduct administration
- This utility is similar to the Remote Desktop feature found in Windows Machine.


### Important things to remember

- Communication between Linux/UNIX and other different computers, networks and remote users is possible.
- The ping command checks whether the connection with a hostname or IP-address is working or not. Run ‘ping IP address or Hostname’ on the terminal
- FTP is preferred protocol for sending and receiving large files. You can establish an - FTP connection to a remote host and then use commands for uploading, downloading files, checking file and browsing them
- Telnet utility helps you to connect to a remote Linux computer and work on it