---
external help file: NTFSSecurity.dll-Help.xml
Module Name: ntfssecurity
online version:
schema: 2.0.0
---

# Remove-Item2

## SYNOPSIS

Deletes the specified items.  The cmdlet can accept paths and filenames with a combined length over 255 characters.

## SYNTAX

```
Remove-Item2 [[-Path] <String[]>] [-Force] [-Recurse] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The Remove-Item2 cmdlet deletes one or more items. 

## EXAMPLES

### Example 1

```PowerShell
PS C:\> Remove-Item2 C:\Test\*.*
```

This example deletes all files with names that include a dot (.) from the C:\Test folder. Because the command specifies a dot, the command doesn't delete folders or files that have no file extension.

### Example 2

```PowerShell
    PS C:\> Remove-Item2 -Path C:\Test\hidden-RO-file.txt -Force
```
This command deletes a file that's both hidden and read-only.
It uses the *Path* parameter to specify the file. It uses the *Force* parameter to delete it. Without *Force*, you can't delete read-only or hidden files.

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

### -Force

Forces the cmdlet to remove items that can't otherwise be changed, such as hidden or read-only files or read-only aliases or variables. The cmdlet can't remove constant aliases or variables. Even using the *Force* parameter, the cmdlet can't override security restrictions.

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

Causes the cmdlet to return the item or items that it removes.

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

### -Path

Specifies a path of the items being removed. Wildcard characters are permitted.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: FullName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Recurse

Indicates that this cmdlet deletes the items in the specified locations and in all child items of the locations.

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

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
