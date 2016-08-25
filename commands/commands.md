# Some Linux Commands

## Shell Commands
* `sudo !!` - run with sudo your previous command
```sh
$ pacman -S emacs
$ sudo !!
```

* `<space> command` - use space before command if you don't want to save command in history

* `reset` - reset your terminal after binary data input or bugs

* `mount | column -t` - print all mounted fs

* `(cd /tmp && ls)` - change directory, execute command and return to the previouse directory.

* `dd if=/dev/dsp | ssh -c arcfour -C username@host dd of=/dev/dsp` - redirect audio from your microphone to the speakers on a remote machine.

* `ssh -N -L2001:localhost:80 somemachine` - create a tunnel from port 80 on the remote machine to the local 2001

* `ALT .` — put the argument of the last command to the console
```sh
$ ls file
$ <press ALT>.
file
```
* `^foo` — run the previous command, but with replacing.
```sh
$ echo "rexezr"
$ ^z
rexer
```

* `man hier` - Show File System Hierarchy

* `fuser -k filename` - Kills a process that is locking a file.

* `cat /etc/issue` - Display which distro is installed

* `sed -n '10,20p' <filename>` - Print all the lines between 10 and 20 of a file

* `ls -R | grep ":$" | sed -e 's/:$//' -e 's/[^-][^\/]*\//--/g' -e 's/^/   /' -e 's/-/|/'` - Graphical tree of sub-directories

* `pv sourcefile > destfile` - Copy a file using pv and watch its progress

* `mkdir -p a/long/directory/path` - Make directory including intermediate directories

* `mkdir /home/foo/doc/bar && cd $_` - mkdir & cd into it as single command

* `du -s * | sort -n | tail` - Get the 10 biggest files/folders for the current direcotry 

* `find -size +100M` - show files which bigger then 100m

* `stat file` - show all statistic info about file

* `file f` - show info about type if file

* `id` - show ids of user

* `> file.txt` - clear, but doesn't delete file

* `du -h -max-depth=1` - show size of subdirictories in human readable format

* `tac file` - reverse cat

* `nl file` - numerate lines of file

* `ss` - show info about sockets

* `last` - show users which logged on system

* `pstree` - show all processes like tree

* `ssh [user]@[server] '[command]'` - run remote command on server by user

* `strace` - debug programm

* `getconf LONG_BIT` - 64 or 32 bit system

* `command | convert label:@- /path/name.png` - save output of `command` in png format

* `host`, `dig` - commands for dns searching

* `bind -p` - show all keyboard binding

* `find . -user user_name` - find all files for user_name(owner)

* `find -size +100M` - find all files which are bigger than 100M in current dir

* `ps aux` - all process info


