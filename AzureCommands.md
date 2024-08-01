## This is an rough note of commands, adding here only for reference

1. **Disbale Az content**,  The Disable-AzContextAutosave -Scope Process command is used in the Azure PowerShell module to disable the automatic saving of Azure context information for the current process.

    `Disable-AzContextAutosave -Scope Process `

     **Azure Context Information**
           When you interact with Azure resources using Azure PowerShell, the context (e.g., subscription, tenant, account information) is saved to enable seamless interaction with 
       multiple commands without needing to repeatedly specify these details.

     **Autosave Mechanism**
         By default, Azure PowerShell uses an autosave mechanism that can save the context information either for the current session (Process), for all sessions (CurrentUser), or globally 
     (AllUsers). This ensures that your context information is preserved across sessions or system-wide.

     **Disabling Autosave for the Current Process**
         Using the -Scope Process parameter specifies that the autosave settings apply only to the current process. Disabling autosave in this context means that any changes to the Azure context during the current PowerShell session will not be automatically saved.

2. **Connect to Azure with system-assigned managed identity**
   `$AzureContext = (Connect-AzAccount -Identity).context`
