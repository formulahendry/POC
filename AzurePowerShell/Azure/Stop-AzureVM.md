---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: 
schema: 2.0.0
---

# Stop-AzureVM
## SYNOPSIS
Shuts down an Azure virtual machine.

## SYNTAX

### ByName (Default)
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

### Input
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

## DESCRIPTION
The Stop-AzureVM cmdlet shuts down a virtual machine.

## EXAMPLES

### --------------------------  Example 1: Shut down a virtual machine  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

This command shuts down a virtual machine that the specified service contains.

### --------------------------  Example 2: Shut down a virtual machine by using a virtual machine object  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

This command shuts down a virtual machine that the specified service contains, by using the virtual machine object that Get-AzureVM returns.

### --------------------------  Example 3: Shut down a VM and keep the VM provisioned  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

This command shuts down a virtual machine that the specified service contains, and keeps it provisioned.

### --------------------------  Example 4: Shut down a VM and allow deallocation of the last VM in the deployment  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

This command shuts down a virtual machine that the specified service contains and allows deallocation of the last virtual machine in the deployment.

### --------------------------  Example 5: Shut down multiple VMs  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

This command shuts down multiple virtual machines that the specified service contains.

## PARAMETERS

### -Name
Specifies the name of the virtual machine to shut down.

Use the wildcard character to stop multiple virtual machines asynchronously.
With a wildcard character, this cmdlet calls the Shutdown Roles operation (http://msdn.microsoft.com/en-us/library/azure/dn469421.aspx), instead of the Shutdown Role operation (http://msdn.microsoft.com/en-us/library/azure/jj157195.aspx).

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StayProvisioned
Specifies that this cmdlet keeps the virtual machine provisioned.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Specifies whether to allow the deallocation of the last virtual machine in a deployment.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Specifies the name of the Azure service that contains the virtual machine to shut down.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -VM
Specifies a virtual machine object that identifies the virtual machine to shut down.

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureVM]()

[New-AzureVM]()

[Restart-AzureVM]()

[Start-AzureVM]()

