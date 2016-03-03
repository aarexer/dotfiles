# Hanging SSH connection.

### Problem:
Sometimes i have annoying bug: 
After than i login to the server by ssh connection, walk away and returning to the computer - i see that my terminal is hanging.

Solution:
Add to the ` ~/.ssh/config:`

```sh
Host *
    TCPKeepAlive yes
    ServerAliveInterval 30
```
