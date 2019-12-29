# powershell-fu
Useful, simple, practical powershell commands

## Open Powershell as administrator in directory
```
alt, f, s, a (while at the directory in File Explorer)
```

## Create an empty file
```
ni myfile
```

## Open File Explorer
```
ii .
```

## Clear the screen
```
clear
```

## List local environment variables
```
Get-ChildItem env:
```

## Use a local environment variable
```
$env:MYVARIABLENAME
```

## Get number of lines/words/characters in a file
```
Get-Content .\myfile | Measure-Object -line
Get-Content .\myfile | Measure-Object -word
Get-Content .\myfile | Measure-Object -character
```

## Set up alias commands
```
$ New-Item -Type file -Path $PROFILE -Force
$ code $PROFILE

# in vscode
function Get-GitStatus { & git status $args }
New-Alias -Name s -Value Get-GitStatus
```

## Restart without exiting
```
. $profile

# or whatever profile you're trying to invoke
. $profile.AllUsersAllHosts
```
