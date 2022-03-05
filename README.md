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

# Networking

## Nmap

Scans ports for a IP address.


# Web

## Gobuster

Enumerates directories for a website

## Nikto

Like gobuster but lists vulnerabilities and other cool stuff.


# Windows

## Enum4Linux

Enumerates Windows stuff running on a machine

## Kerbrute

Brute forces active directory


# Wi-Fi Hacking

## Get Hash from capture

https://www.onlinehashcrack.com/tools-cap-to-hash-converter.php

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
