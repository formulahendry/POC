---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
online version: 
schema: 2.0.0
---

# Submit-AzureRmDataLakeAnalyticsJob
## SYNOPSIS
Submits a job.

## SYNTAX

### Submit SQL-IP Job
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

### Submit job with script path for SQL-IP
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

## DESCRIPTION
The Submit-AzureRmDataLakeAnalyticsJob cmdlet submits an Azure Data Lake Analytics job.

## EXAMPLES

### --------------------------  Example 1: Submit a job  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\> Submit-AzureRmDataLakeAnalyticsJob -AccountName "ContosoAdlAccount" `
                   -Name "New Job" -ScriptPath $localScriptPath `
                   -DegreeOfParallelism 32
```

This command submits a Data Lake Analytics job.

## PARAMETERS

### -Account
Specifies the Data Lake Analytics account name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: 
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifies the job name.

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

### -ScriptPath
Specifies the local file path to the script to run.

```yaml
Type: String
Parameter Sets: Submit job with script path for SQL-IP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Runtime
Specifies the runtime version of the job.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CompileMode
Specifies the compilation mode of the job.
The acceptable values for this parameter are:

-- Semantic
-- Full
-- SingleBox

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CompileOnly
Indicates that this cmdlet compiles the job without running it.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DegreeOfParallelism
Specifies the Data Lake Analytics Units (DLAU) of the job, which indicates the maximum allowable parallelism of the job.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority
Specifies the priority of the job.
If not specified, the priority is 1000.
A lower the number indicates a higher job priority.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
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

### -Script
Specifies the contents of the script to run.

```yaml
Type: String
Parameter Sets: Submit SQL-IP Job
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureRmDataLakeAnalyticsJob]()

[Stop-AzureRmDataLakeAnalyticsJob]()

[Wait-AzureRmDataLakeAnalyticsJob]()

