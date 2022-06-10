# OG Hacker Tools
This repository contains tools used for various types of hacking, and basic information about their usage.

# Reverse Engineering

## Radare2 aka R2

Typical usage:
`r2 -A -d <program_name>`

-A: Equivalent to aaa inside r2

-d: Enables debug mode

### Nice commands inside r2:

afl: Lists all the functions

izz: lists all the strings in the binary

pdf @<function_name>: Disassembles respective function

px: prints current position in memory in hexadecimal

db: defines breakpoing

dc: Runs the program untill next breakpoint

## JD-GUI

Allows you to see the Java Source Code, from .class file

## Java Deobfuscator

Can deobfuscate a Java Archive File aka .jar

Usage, change the detect.yml to: 
`input: <file_name>.jar
detect: true`

Usage:
`java -jar deobfuscator.jar --config detect.yml`

## Floss

Deobfucates strings, its like the command strings, but for obfuscated strings.

## ILSpy

Reverse Engineer for .NET applications

## dotPeek

Reverse Engineer for .NET applications

## MobSF

Application that analyses a Android APK in a automated manner

## Pithus

Website that analyses a Android APK in a automated manner


# Networking

## Nmap

Scans ports for a IP address.

# Web

## Gobuster

Enumerates directories for a website

## Nikto

Like gobuster but lists vulnerabilities and other cool stuff.

## Wfuzz

Web Fuzzer, brute force for web applications

Usage:
`wfuzz -c -z file,<wordlist> http://www.example.site/api/FUZZ`

Being FUZZ the place, where the tool places the contents of the wordlist

# Windows

## Enum4Linux

Enumerates Windows stuff running on a machine

## Kerbrute

Brute forces active directory

## SMBMap

Detects and exploits Samba vulnerabilities

## Impacket

Series of scripts that gets you inside a Windows Machine


# Wi-Fi Hacking

## Get Hash from capture

https://www.onlinehashcrack.com/tools-cap-to-hash-converter.php


# SQL Injection

## SQLMap 

Detects and exploits SQL Injection vulnerabilities

# Steganography

## Stegoveritas

VERY GOOD! Swiss army knife for steganography

Usage:
`stegoveritas <filename>`


## Stegcracker

Used to crack passwords for content inside images

## Strings

Lists all strings inside a file

## Binwalk

Lists all the files inside other file

Typical usage:
`binwalk -e <filename>`

-e: Extracts all the files inside the other file


## Steghide

Hide information inside .jpg files

Extract:
`steghide extract -sf <filename>`

## Zsteg

Like Steghide, but for .png files

Usage:
`zsetg <filename>`

## Exiftool

See and edit metadata in images

Usage:
`exiftool <filename>`

## Sonic Visualizer 

See and edit sound waves of audio files

## Academo - Spectrum Analyzer
Great to find hidden message in the audio waves
https://academo.org/demos/spectrum-analyzer/

# OSInt

## Sherlock

OSInt tool that searches for usernames on the open internet

## WhatsMyName

Another tool that searches for usernames on the open internet

## Wiggle

Website that contains a lot of public Wifi and their locations


