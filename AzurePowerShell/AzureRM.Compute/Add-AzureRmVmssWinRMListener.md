---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: 
schema: 2.0.0
---

# Add-AzureRmVmssWinRMListener
## SYNOPSIS
Adds a WinRM listener to the VMSS.

## SYNTAX

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

## DESCRIPTION
This cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).

## EXAMPLES

### --------------------------  Example 1: Add a WinRM listener to the VMSS  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>$VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

This example adds a WinRM listener to the VMSS.

## PARAMETERS

### -VirtualMachineScaleSet
Specifies the VMSS object.
You can use the New-AzureRmVmssConfig cmdlet to create the object.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Protocol
Specifies the protocol of the WinRM listener.
The acceptable values for this parameter are:

-- Http
-- Https

```yaml
Type: ProtocolTypes
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl
Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### This cmdlet does not generate any output.

## NOTES

## RELATED LINKS

[New-AzureRmVmssConfig]()

