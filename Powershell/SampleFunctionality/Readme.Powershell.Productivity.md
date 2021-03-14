Powershell Productivity tips usecases 
======================


* Copy history of cmdlets to Clipboard 
    - `Get-History -Count 46 | Set-Clipboard`
        - This is very helpful to document one time experiments
* Get list of commands 
    - `Get-Command -Module Az.Automation`
* How to assign a variable with multiple special characters
``` 
$var= @"
{"instname":"MySQLInstance","version":"12.0.6433.1","patchstatus":"current"}
"@
```
* Easiest way to keep track of Powershell console output, using transcript (Loggin)
    - Consider using [PowerShellLogging module](https://www.powershellgallery.com/packages/PowerShellLogging/1.3.0)
    - Alternative option is to use Transcript , sample listed below
```
Start-Transcript "Transcript_$(Get-Date -f MM-dd-yyyy_HHmmss).txt"
Stop-transcript 
```



Modele related
--------------
* Importing a module 
    - `Import-Module Az.Automation`
* Install a module with given version
    - `Install-Module -Name AzureRM.Automation -MaximumVersion 6.1.1`
* How to find all repositories configured, that will be used during Intall-module
    - `Get-PSRepository`
* How to register default Repository
    - `Register-PSRepository -Default -Verbose`
        - Sampel output 
```  
VERBOSE: Performing the operation "Register Module Repository." on target "Module Repository 'PSGallery' () in provider
 'PowerShellGet'.".
VERBOSE: Repository details, Name = 'PSGallery', Location = 'https://www.powershellgallery.com/api/v2'; IsTrusted =
'False'; IsRegistered = 'True'.
```        
* Find a module in Repo
    - `Find-Module -Name AzureRM.Automation`
        - Workaround that helped with error - `WARNING: Unable to resolve package source 'https://www.powershellgallery.com/api/v2'`
            - `[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12` -> Ref: https://www.powershellcenter.com/2020/08/27/powershell-fix-warning-unable-to-resolve-package-source-https-www-powershellgallery-com-api-v2/
* Uninstall a module
    - `Get-Module AzureRM.profile -ListAvailable | Uninstall-Module`
* Trust Gallary
    - `Set-PSRepository -Name "PSGallery" -InstallationPolicy Trusted`