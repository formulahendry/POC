---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
online version: http://go.microsoft.com/fwlink/?LinkId=690300
schema: 2.0.0
---

# Remove-AzureKeyVaultSecret
## SYNOPSIS
Deletes a secret in a vault.

## SYNTAX

```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## DESCRIPTION
The Remove-AzureKeyVaultSecret cmdlet deletes a secret in an Azure Key Vault instance.
This cmdlet has a value of high for the ConfirmImpact property.

## EXAMPLES

### Example 1: Remove a secret from a vault
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

This command removes the secret named FinanceSecret from the vault named Contoso.

### Example 2: Remove a secret from a vault without user confirmation
```
PS C:\>Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

This command removes the secret named FinanceSecret from the vault named Contoso.
The command specifies the Force and Confirm parameters, and, therefore, the cmdlet does not prompt you for confirmation.

## PARAMETERS

### -Force
Forces the command to run without asking for user confirmation.

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

### -Name
Specifies the name of a secret.
This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the vault, and your current environment.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Indicates that this cmdlet returns a Microsoft.Azure.Commands.KeyVault.Models.Secret object.
By default, this cmdlet does not generate any output.

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

### -VaultName
Specifies the name of the vault to which the secret belongs.
This cmdlet constructs the FQDN of a vault based on the name that this parameter specifies and your current environment.

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

### String

## OUTPUTS

### Microsoft.Azure.Commands.KeyVault.Models.Secret
This cmdlet returns a value only if you specify the PassThru parameter.

## NOTES

## RELATED LINKS

[Get-AzureKeyVaultSecret]()

[Set-AzureKeyVaultSecret]()

