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

## Delete a file
```
rm myfile
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
get-childitem env:
```

## Use a local environment variable
```
$env:MYVARIABLENAME
```

## Get number of lines/words/characters in a file
```
get-content .\myfile | measure-object -line
get-content .\myfile | measure-object -word
get-content .\myfile | measure-object -character
```

## Set up alias commands
This sets up `gs` as `git status`
```
$ New-Item -Type file -Path $PROFILE -Force
$ code $PROFILE

# in vscode
function Get-GitStatus { & git status $args }
New-Alias -Name gs -Value Get-GitStatus
```

## Find out what command an alias is doing
```
get-alias myalias
```

## Restart without exiting
```
. $profile

# or whatever profile you're trying to invoke
. $profile.AllUsersAllHosts
```
