# ```copy-item```
Copy-Item .\module\ 1023 -Recurse
this cmdlet can copy the content in module to directory 1023
Copy-Item .\module\* 1023 -Recurse 
the character * can not add the directory name



This example copies the contents of the C:\Logfiles directory into the existing C:\Drawings directory. The Logfiles directory isn't copied.

If the Logfiles directory contains files in subdirectories, those subdirectories are copied with their file trees intact. 
By default, the Container parameter is set to True, which preserves the directory structure.

# Pay attention to the difference
## ```Copy-Item -Path "C:\Logfiles\*" -Destination "C:\Drawings" -Recurse```

If you need to include the Logfiles directory in the copy, remove the \* from the Path. For example:

## ```Copy-Item -Path "C:\Logfiles" -Destination "C:\Drawings" -Recurse ```

I can get the procedure to install powershell in raspberry pi4
https://www.cnblogs.com/shanyou/p/6287890.html

# ``` Start-Process -FilePath "powershell" -Verb RunAs ```
This example starts PowerShell by using the Run as administrator option.

#  ``` about_Execution_Policies ``` problem
The default Execution_Policy is Restricted.So you need to do eleminate the restriction by manual.
``` Set-ExecutionPolicy -ExecutionPolicy Unrestricted ``` Then press Y

# ``` ls | Where-Object { $_.Mode.Substring(0,1) -eq 'd'} | ls | ForEach-Object {$_.Name} ```
show all items of the child directory

# ``` Get-ChildItem -Recurse -Filter *.json```
This cmdlet helps us get same type files

# ``` New-NetFirewallRule ```
new a firewall rule
# $PROFILE indictates the default powershell script file path
add the content to support "UTF-8"

```
$OutputEncoding = [console]::InputEncoding = [console]::OutputEncoding = New-Object System.Text.UTF8Encoding 
```

# ``` Read-Host ```
Read the parameters from the input of the user and differs from the beginging input
we can access the value by ```$args[index]```

# ```$OutputEncoding = [console]::InputEncoding = [console]::OutputEncoding = New-Object System.Text.UTF8Encoding```
set the powershell as UTF-8.And you must add the former content to $PROFILE.
# This link indicates the Remove-item high-level functions
[link](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/remove-item?view=powershell-7.1)

# close the monitor

```
(Add-Type '[DllImport("user32.dll")]public static extern int SendMessage(int hWnd, int hMsg, int wParam, int lParam);' -Name a -Pas)::SendMessage(-1,0x0112,0xF170,2)
```
# test the net port
`netsh interface ipv4 show excludedportrange protocol=tcp`