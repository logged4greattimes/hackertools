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
