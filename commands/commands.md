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
