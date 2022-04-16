## PowerShell.Module.TakeOwnership
<#
    .SYNOPSIS
        Cmdlet to do simple management of Windows permissions.
             
    .DESCRIPTION
        Cmdlet to do simple management of Windows permissions for different object types:
    .PARAMETER Path
    .PARAMETER Recurse
    .PARAMETER ObjectType
        File    Directory/file
        reg     Registry key
        srv     Service
        shr     Network share
        wmi     WMI objec
    .EXAMPLE
        Grant-Ownership 'c:\MyTest'
        Grant-Ownership 'c:\MyTest' -Recurse
        Grant-Ownership 'HKCU\SOFTWARE\CodeCastor\Test' -ObjectType registry
    .Notes
        REGISTRY VALUE
        HKEY_CURRENT_USER\SOFTWARE\Classes\Directory\shell\TakeOwn\command
        pwsh.exe -noni -nol -nop -c "& { Start-Process -Verb RunAs -FilePath "pwsh.exe" -ArgumentList '-noni -nol -nop -c "& { C:\Scripts\powershell-sandbox\TakeOwn\TakeOwn.ps1 "%1" ; Sleep 5 ;}"' }"
 #>
