---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: 
schema: 2.0.0
---

# Stop-AzureRmVmss
## SYNOPSIS
Stops the VMSS or a set of virtual machines within the VMSS.

## SYNTAX

### InvokeByDynamicParameters (Default)
```
Stop-AzureRmVmss [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
```

### InvokeByDynamicParametersForFriendMethod
```
Stop-AzureRmVmss [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-StayProvisioned]
```

### InvokeByStaticParametersForFriendMethod
```
Stop-AzureRmVmss [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-StayProvisioned]
```

## DESCRIPTION
The Stop-AzureRmVmss cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.
You can use the InstanceId parameter to select a set of virtual machines.

## EXAMPLES

### --------------------------  Example 1: Stop all the virtual machines within the VMSS  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

This command stops all virtual machines that belong to the VMSS named ContosoVMSS.

### --------------------------  Example 2: Stop a specific set of virtual machines within the VMSS  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.

## PARAMETERS

### -InformationAction
@{Text=}

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
@{Text=}

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of the resource group of the VMSS.

```yaml
Type: String
Parameter Sets: InvokeByDynamicParameters, InvokeByDynamicParametersForFriendMethod
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Specifies the name of the VMSS for which this cmdlet stops the virtual machines.

```yaml
Type: String
Parameter Sets: InvokeByDynamicParameters, InvokeByDynamicParametersForFriendMethod
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.
For instance: -InstanceId "0", "3".

```yaml
Type: String[]
Parameter Sets: InvokeByDynamicParameters, InvokeByDynamicParametersForFriendMethod
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StayProvisioned
Indicates that this cmdlet deallocates all the virtual machines within the VMSS so that the user is not charged for the stopped virtual machines.

```yaml
Type: SwitchParameter
Parameter Sets: InvokeByDynamicParametersForFriendMethod, InvokeByStaticParametersForFriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureRmVmss]()

[New-AzureRmVmss]()

[Remove-AzureRmVmss]()

[Restart-AzureRmVmss]()

[Set-AzureRmVmss]()

[Start-AzureRmVmss]()

[Update-AzureRmVmss]()

