---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-AzureVMImageDiskConfigSet
## SYNOPSIS
Creates a disk configuration set object.

## SYNTAX

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

## DESCRIPTION
The New-AzureVMImageDiskConfigSet cmdlet creates a disk configuration set object that is passed to the image update cmdlet.
It encapsulates the OSDiskConfig and the DataDiskConfig object.
Use the Set-AzureVMImageOSDiskConfig and Set-AzureVMImageDataDiskConfig cmdlets to set the OS Disk and Data Disk properties for the virtual machine image.

## EXAMPLES

### --------------------------  Example 1: Create a disk configuration set object  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>$Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

This command creates a disk configuration set object and stores the results in the variable named $Disk.
After the disk configuration is created, it is used to set the OSDiskConfig and DataDiskConfig.
Then the virtual machine is updated with the configuration.

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

## INPUTS

## OUTPUTS

### Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet

## NOTES

## RELATED LINKS

[Get-AzureVMImageDiskConfigSet]()

[Set-AzureVMImageOSDiskConfig]()

[Set-AzureVMImageDataDiskConfig]()

