# powershell-fu
Useful, simple, practical powershell commands

## List local environment variables
Get-ChildItem env:

## Use a local environment variable
$env:MYVARIABLENAME

## Get number of lines in a file
Get-Content .\myfile | Measure-Object -line

## Get number of words in a file
Get-Content .\myfile | Measure-Object -word

## Get number of characters in a file
Get-Content .\myfile | Measure-Object -character
