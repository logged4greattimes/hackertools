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

## Static Binaries

https://github.com/andrew-d/static-binaries

## Malware Analysis

PECheck - See info on PEHeader

PETree - See info on PeHeader in a GUI

Cuckoo Sandbox - https://cuckoosandbox.org/ 

REMnux - Distro for analysis of malware


## Red Team Toolkit

https://github.com/infosecn1nja/Red-Teaming-Toolkit#Payload%20Development
