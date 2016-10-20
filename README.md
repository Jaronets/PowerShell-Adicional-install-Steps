# PowerShell-Adicional-install-Steps
Pasos Adicionales para instalar Power Shell con Azure
PROBLEMA DE INSTALACION DE MODULOS EN POWERSHELL

PS C:\windows\system32> Install-Module AzureRM
Install-Module : The 'Install-Module' command was found in the module 'PowerShellGet', but the module could not be loaded. For more information, run 'Import-Module 
PowerShellGet'.
At line:1 char:1
+ Install-Module AzureRM
+ ~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Install-Module:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CouldNotAutoloadMatchingModule
 

PS C:\windows\system32> Install-Module AzureRM
Install-Module : The 'Install-Module' command was found in the module 'PowerShellGet', but the module could not be loaded. For more information, run 'Import-Module 
PowerShellGet'.
At line:1 char:1
+ Install-Module AzureRM
+ ~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Install-Module:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CouldNotAutoloadMatchingModule


http://go.microsoft.com/fwlink/?LinkID=135170.

PS C:\windows\system32> Get-ExecutionPolicy 
Restricted

PS C:\windows\system32> Get-ExecutionPolicy -list

        Scope ExecutionPolicy
        ----- ---------------
MachinePolicy       Undefined
   UserPolicy       Undefined
      Process       Undefined
  CurrentUser       Undefined
 LocalMachine       Undefined
 

PS C:\windows\system32> Get-ExecutionPolicy -Scope CurrentUser
Undefined

PS C:\windows\system32> Import-Module PowerShellGet
Import-Module : File C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1 cannot be loaded because running scripts is disabled on this system. 
For more information, see about_Execution_Policies at http://go.microsoft.com/fwlink/?LinkID=135170.
At line:1 char:1
+ Import-Module PowerShellGet
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : SecurityError: (:) [Import-Module], PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess,Microsoft.PowerShell.Commands.ImportModuleCommand

PS C:\windows\system32> Set-ExecutionPolicy RemoteSigned

PS C:\windows\system32> Import-Module PowerShellGet

PS C:\windows\system32> Install-Module AzureRM

PS C:\windows\system32> Install-Module Azure

PS C:\windows\system32> Set-ExecutionPolicy Restricted

PS C:\windows\system32> 
