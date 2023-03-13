---
external help file: NTFSSecurity.dll-Help.xml
Module Name: ntfssecurity
online version:
schema: 2.0.0
---

# Disable-NTFSAccessInheritance

## SYNOPSIS

Disables NTFS access control list inheritance on the specified directory.  

## SYNTAX

### Path (Default)
```
Disable-NTFSAccessInheritance [[-Path] <String[]>] [-RemoveInheritedAccessRules] [-PassThru]
 [<CommonParameters>]
```

### SecurityDescriptor
```
Disable-NTFSAccessInheritance [-SecurityDescriptor] <FileSystemSecurity2[]> [-RemoveInheritedAccessRules]
 [-PassThru] [<CommonParameters>]
```

## DESCRIPTION

Disables NTFS access control list inheritance on the specified directory.  By default will convert the existing access control entries to explicit entries.

## EXAMPLES

### Example 1

```PowerShell
PS C:\> Disable-NTFSAccessInheritance -path d:\my\dir
```

In a directory tree "d:\my\dir\tree", ntfs access inheritance will be broken at "dir".  The child directory "tree" will still inherit from its parent.

## PARAMETERS

### -PassThru

{{ Fill PassThru Description }}

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

The path of the directory where NTFS access inheritance will be disabled

```yaml
Type: String[]
Parameter Sets: Path
Aliases: FullName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -RemoveInheritedAccessRules

Removes any inherited access control entries, leaving any existing explicit entries in place.

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

### -SecurityDescriptor

The SecurityDescriptor parameter allows passing an security descriptor or an array or security descriptors.

A security descriptor contains information about the owner of the object, and the primary group of an object. The security descriptor also contains two access control lists (ACL). The first list is called the discretionary access control lists (DACL), and describes who should have access to an object and what type of access to grant. The second list is called the system access control lists (SACL) and defines what type of auditing to record for an object.

```yaml
Type: FileSystemSecurity2[]
Parameter Sets: SecurityDescriptor
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String[]

### Security2.FileSystemSecurity2[]

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
