---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureRmVMImageOffer
## SYNOPSIS
Gets VMImage offer types.

## SYNTAX

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>]
```

## DESCRIPTION
The Get-AzureRmVMImageOffer cmdlet gets the VMImage offer types.

## EXAMPLES

### --------------------------  Example 1: Get offer types for a publisher  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

This command gets the offer types for the specified publisher in the Central US region.

## PARAMETERS

### -Location
Specifies the location of the VMImage.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublisherName
Specifies the name of a publisher of a VMImage.
To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

## NOTES

## RELATED LINKS

[Get-AzureRmVMImage]()

[Get-AzureRmVMImagePublisher]()

[Get-AzureRmVMImageSku]()

[Save-AzureRmVMImage]()

