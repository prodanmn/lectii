# WINDOWS


## WINDOWS commands 
* [windows-commands](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/cmd)

|command | description |
| - | - 
`MOVE *.pdf` d:\recovery | move all pdf files in recovery folder
`dir "search term*" /s` | search file
`dir /a:h` | find hidden filles
`DEL . DR` | delete all directories
`sc delete servicename` | delete servicename

### Example commands
#### Remove last caracter
```cmd
@echo off
setlocal enabledelayedexpansion
set /P FOLDER_PATH=
for %%f in (%FOLDER_PATH%*) do if %%f neq %~nx0 (
    set "filename=%%~nf"
    ren "%%f" "!filename:~0,-1!%%~xf"
)
```
