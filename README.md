# OG Hacker Tools
This repository contains tools used for various types of hacking, and basic information about their usage.

## Upgrade Shell

### Option 1
``` 
python3 -c 'import pty;pty.spawn("/bin/bash")'
export TERM=xterm
stty raw -echo; fg
```

### Option 2
```
rlwrap nc -lvnp 9001
stty raw -echo; fg
```


## Red Team Toolkit

https://github.com/infosecn1nja/Red-Teaming-Toolkit#Payload%20Development
