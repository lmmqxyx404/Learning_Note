# ```copy-item```
Copy-Item .\module\ 1023 -Recurse
this cmdlet can copy the content in module to directory 1023
Copy-Item .\module\* 1023 -Recurse 
the character * can not add the directory name



This example copies the contents of the C:\Logfiles directory into the existing C:\Drawings directory. The Logfiles directory isn't copied.

If the Logfiles directory contains files in subdirectories, those subdirectories are copied with their file trees intact. 
By default, the Container parameter is set to True, which preserves the directory structure.

Copy-Item -Path "C:\Logfiles\*" -Destination "C:\Drawings" -Recurse

If you need to include the Logfiles directory in the copy, remove the \* from the Path. For example:

Copy-Item -Path "C:\Logfiles" -Destination "C:\Drawings" -Recurse

I can get the procedure to install powershell in raspberry pi4
https://www.cnblogs.com/shanyou/p/6287890.html

# ``` Start-Process -FilePath "powershell" -Verb RunAs ```
This example starts PowerShell by using the Run as administrator option.

# $PROFILE indictates the default powershell script file path