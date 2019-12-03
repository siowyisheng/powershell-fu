# powershell-fu
Useful, simple, practical powershell commands

## Get number of lines in a file
Get-Content .\myfile | Measure-Object -line

## Get number of words in a file
Get-Content .\myfile | Measure-Object -word

## Get number of characters in a file
Get-Content .\myfile | Measure-Object -character
