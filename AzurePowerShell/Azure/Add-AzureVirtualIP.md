---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: 
schema: 2.0.0
---

# Add-AzureVirtualIP
## SYNOPSIS
Adds a virtual IP to a cloud service.

## SYNTAX

```
Add-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

## DESCRIPTION
The Add-AzureVirtualIP cmdlet adds a new virtual IP (VIP) to your Azure service.
The new virtual IP has a name but is not allocated an IP address.

The IP address is allocated only when you associate an endpoint to the VIP.
See Add-AzureEndpoint for more details.

Your subscription is charged for extra VIPs only once they are associated with an endpoint.

## EXAMPLES

### --------------------------  Example 1: Add a virtual IP to a service  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Add-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
OperationDescription OperationId                          OperationStatus
-------------------- -----------                          ---------------
Add-AzureVirtualIP   4bd7b638-d2e7-216f-ba38-5221233d70ce Succeeded
```

This command adds a virtual IP address to a service.

## PARAMETERS

### -ServiceName
Specifies the name of the service.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualIPName
Specifies the name of the virtual IP address.

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

### Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext

## NOTES

## RELATED LINKS

[Add-AzureEndpoint]()

[Remove-AzureVirtualIP]()

