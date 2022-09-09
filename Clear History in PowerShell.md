# Clear History in PowerShell

## Get the PowerShell command history file location:
```
(Get-PSReadlineOption).HistorySavePath
```


## Show the contents of the PowerShell command history file:
```
PS C:\> cat (Get-PSReadlineOption).HistorySavePath
```


## Clear the command history in PowerShell by deleting the history file:
```
PS C:\> Remove-Item (Get-PSReadlineOption).HistorySavePath
```


## Change how PowerShell command history is saved:
```
PS C:\> Set-PSReadlineOption -HistorySaveStyle SaveIncrementally # default
PS C:\> Set-PSReadlineOption -HistorySaveStyle SaveAtExit
PS C:\> Set-PSReadlineOption -HistorySaveStyle SaveNothing
```
