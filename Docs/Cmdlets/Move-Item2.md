---
external help file: NTFSSecurity.dll-Help.xml
Module Name: ntfssecurity
online version:
schema: 2.0.0
---

# Move-Item2

## SYNOPSIS

Moves one or more items to a new location, without the 255 character path and filename limit.

## SYNTAX

```
Move-Item2 [-Path] <String[]> [-Destination] <String> [-Force] [-PassThru <Boolean>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The Move-Item2 cmdlet moves one or more items, including its properties, contents, and childitems, to a new location. The items can be files, folders, or a combination of both. Both the source and destination paths can be over 255 characters long. The cmdlet can also be used to rename items. 

Moved items are added to the new loction and removed from the original location. If the destination location already contains an item with the same name as the item being moved, the cmdlet prompts you for confirmation before overwriting the existing item. To overwrite the existing item without being prompted, use the Force parameter.

## EXAMPLES

### Example 1

```PowerShell
PS C:\> Move-Item2 -Path C:\test.txt -Destination E:\Temp\tst.txt
```

This command moves the Test.txt file from the C: drive to the E:\Temp directory and renames it from test.txt to tst.txt.

### Example 2

```PowerShell
PS C:\> Move-Item2 -Path C:\Temp -Destination C:\Logs
```

This command moves the C:\Temp directory and its contents to the C:\Logs directory. The Temp directory, and all of its subdirectories and files, then appear in the Logs directory.

## PARAMETERS

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Destination

Specifies the path to the new location of the item. The new location can be a folder or a file name. If the destination is a folder, the item is moved to the folder and retains its original name. If the destination is a file name, the item is moved to the folder and renamed to the file name.  The default value is the current directory.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force

{{ Fill Force Description }}

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

### -PassThru

{{ Fill PassThru Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path

Specifies the path to the current location of the items. The default is the current directory. Wildcard characters are permitted.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String[]

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
