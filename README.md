# Asynchronous-Directory-Manager
Mimic file/directory changes on a local directory onto a specified remote directory on another server
-------------------------------------------------------------------------------
### Usage
1. git clone https://github.com/Azoam/Asynchronous-Directory-Manager.git
2. (optional). Alias or put into your Path variable the command 'node <absolute path to index.js>' as adm
3. Go into the directory where you would like changes to be recorded and mimiced.
4. Run:
```adm``` (or ```node <absolute path to index.js>``` if you skipped 2) ```--host <hostname, ilab if you want to use an ilab machine> --remote <remote directory on the specified host>```
5. You will be prompted for the ssh username and password (make sure your host machine allows for ssh, the program is scp based)
6. As the program runs, work on the directory you ran the command in and all changes should be done on the remote directory you specified.
(TIP): You can run the command in the background to continue use of your bash environment

### Description
- Problem: Lots of people enjoy using their text editors on their local pc's and it's a
bit of a hassle to manage files/directories on remote servers.
- Possible Solution: A Asynchronous Manager that watches the directory being
worked on and whenever any changes happens within that directory (and sub directories)
and applies those changes to a relative remote directory; in a sense mimics.
- Primary Audience: Rutgers Computer Science students, hence ilab.js  
- usage: node index.js --host <hostname of remote server> --remote <absolute path on remote server>

Options|Description|Status
--------|-----|----
host|host to copy files to|Done
remote|absolute directory on relative machine to save files to|Done
mute|remove all verbose output|Done
roe|restarts program on any error|Not Done
debug|prints all error statements|Done
