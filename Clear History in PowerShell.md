# Clear History in PowerShell

<details>
  <summary>Extra Info</summary>
This is not obvious, but the ```Clear-History``` command in PowerShell won’t clear the history of the previous commands.

The ```Clear-History``` clears only the commands entered during the current session, that could be displayed by the ```Clear-History``` command.

To clear the history in PowerShell, it needs to delete the file in which the previous commands are stored.

Below are the steps on how to locate the history file and how to clear the history of the PowerShell commands.
</details>

## Get the PowerShell command history file location:
```
(Get-PSReadlineOption).HistorySavePath
```


## Show the contents of the PowerShell command history file:
```
cat (Get-PSReadlineOption).HistorySavePath
```


## Clear the command history in PowerShell by deleting the history file:
```
Remove-Item (Get-PSReadlineOption).HistorySavePath
```


## Change how PowerShell command history is saved:
```
Set-PSReadlineOption -HistorySaveStyle SaveIncrementally # default
Set-PSReadlineOption -HistorySaveStyle SaveAtExit
Set-PSReadlineOption -HistorySaveStyle SaveNothing
```
