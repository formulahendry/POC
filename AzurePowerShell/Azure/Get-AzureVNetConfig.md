---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureVNetConfig
## SYNOPSIS
Gets the Azure virtual network configuration from the current subscription.

## SYNTAX

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

## DESCRIPTION
The Get-AzureVNetConfig cmdlet retrieves the virtual network configuration of the current Azure subscription.
If the ExportToFile parameter is specified, a network configuration file is created.

## EXAMPLES

### --------------------------  Example 1: Get the virtual network configuration of a current Azure subscription  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Get-AzureVNetConfig
```

This command gets the virtual network configuration of the current Azure subscription and displays it.

### --------------------------  Example 2: Get the virtual network configuration of the current Azure subscription and save it to a local file  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

This command gets the virtual network configuration of the current Azure subscription and then saves it to a local file.

## PARAMETERS

### -ExportToFile
Specifies the path and file name of a network configuration file to be created from the settings.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifies the Azure profile from which this cmdlet reads.
If you do not specify a profile, this cmdlet reads from the local default profile.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureVNetSite]()

[Remove-AzureVNetConfig]()

[Set-AzureVNetConfig]()

