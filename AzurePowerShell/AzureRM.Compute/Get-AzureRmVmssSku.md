---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureRmVmssSku
## SYNOPSIS
Gets the available SKUs for the VMSS.

## SYNTAX

```
Get-AzureRmVmssSku [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [-ResourceGroupName] <String> [-VMScaleSetName] <String>
```

## DESCRIPTION
The Get-AzureRmVmssSku cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).

## EXAMPLES

### --------------------------  Example 1: Get all available SKUs from the VMSS  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.

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
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Species the name of the VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

### This cmdlet does not produce any output.

## NOTES

## RELATED LINKS

[Get-AzureRmVmss]()

