---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
online version: http://go.microsoft.com/fwlink/?LinkId=690162
schema: 2.0.0
---

# Remove-AzureRmKeyVault
## SYNOPSIS
Deletes an Azure Key Vault instance.

## SYNTAX

```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [-Force] [-WhatIf] [-Confirm]
```

## DESCRIPTION
The Remove-AzureRmKeyVault cmdlet deletes the specified Azure Key Vault instance.
It also deletes all keys and secrets contained in that instance.

Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.

## EXAMPLES

### Example 1: Remove a key vault
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

This command removes the key vault named Contoso03Vault from your current subscription.

### Example 2: Remove a key vault from a specified resource group
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

This command removes the key vault named Contoso03Vault from the named resource group.
If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.

## PARAMETERS

### -Force
Indicates that the cmdlet does not prompt you for confirmation.
By default, this cmdlet prompts you to confirm that you want to delete the key vault.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the name of a resource group.

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

### -VaultName
Specifies the name of the key vault to remove.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureRmKeyVault]()

[New-AzureRmKeyVault]()

