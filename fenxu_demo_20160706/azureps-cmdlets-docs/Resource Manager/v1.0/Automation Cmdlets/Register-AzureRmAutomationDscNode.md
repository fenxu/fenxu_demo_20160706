---
external help file: RMAzure_Automation.xml
online version: 19472f94-5827-4878-a17a-d7bb10932861
schema: 2.0.0
source_branch: master
source_repo: https://github.com/Visual-Studio-China/azure-powershell-docs-int
---

# Register-AzureRmAutomationDscNode
## SYNOPSIS
Registers an azure_2 virtual machine as a DSC node for an Automation account.

## SYNTAX

```
Register-AzureRmAutomationDscNode [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-ActionAfterReboot] [-AllowModuleOverwrite <Boolean>] [-AzureVMLocation <String>]
 [-AzureVMResourceGroup <String>] [-ConfigurationMode] [-ConfigurationModeFrequencyMins <Int32>]
 [-NodeConfigurationName <String>] [-RebootNodeIfNeeded <Boolean>] [-RefreshFrequencyMins <Int32>]
 -AzureVMName <String>
```

## DESCRIPTION
The **Register-AzureRmAutomationDscNode** cmdlet registers an azure_2 virtual machine as an APS Desired State Configuration (DSC) node in an azure_2 Automation account.

## EXAMPLES

### Example 1: Register an Azure virtual machine as an Azure DSC node
```
PS C:\>Register-AzureAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

This command registers the azure_2 virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.

## PARAMETERS

### -ActionAfterReboot
Specifies the action that the virtual machine takes after it restarts.
Valid values are: 

-- ContinueConfiguration 
-- StopConfiguration

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -AllowModuleOverwrite
Specifies whether new configurations that this DSC node downloads from the azure_2 Automation DSC pull server replace the existing modules already on the target node.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -AutomationAccountName
Specifies the name of an Automation account in which this cmdlet registers a virtual machine.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMLocation
Specifies the location in which this cmdlet registers a virtual machine.
To obtain valid locations, use the Get-AzureRMLocation cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMName
Specifies the name of the azure_2 virtual machine that this cmdlet registers for management.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMResourceGroup
Specifies the name of the resource group of the azure_2 virtual machine that this cmdlet registers.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationMode
Specifies the DSC configuration mode.
Valid values are: 

-- ApplyAndMonitor 
-- ApplyAndAutocorrect 
-- ApplyOnly

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationModeFrequencyMins
Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -NodeConfigurationName
Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from azure_2 Automation DSC.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -RebootNodeIfNeeded
Specifies whether to restart the virtual machine, if needed.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -RefreshFrequencyMins
Specifies the frequency, in minutes, at which the local Configuration Manager contacts the azure_2 Automation DSC pull server to download the latest node configuration.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of a resource group.
The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureRmAutomationDscNode](19472f94-5827-4878-a17a-d7bb10932861)

[Set-AzureRmAutomationDscNode](68da8fba-38df-4255-91e8-513635163d57)

[Unregister-AzureRmAutomationDscNode](159d4e1d-b8db-4544-9807-c09e63fbd5dd)


