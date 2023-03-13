---
external help file: NTFSSecurity.dll-Help.xml
Module Name: ntfssecurity
online version:
schema: 2.0.0
---

# Enable-NTFSAccessInheritance

## SYNOPSIS

Enables NTFS Access Control List inheritance on the directory specified in the Path parameter.

## SYNTAX

### Path (Default)
```
Enable-NTFSAccessInheritance [[-Path] <String[]>] [-PassThru] [-RemoveExplicitAccessRules] [<CommonParameters>]
```

### SecurityDescriptor
```
Enable-NTFSAccessInheritance [-SecurityDescriptor] <FileSystemSecurity2[]> [-PassThru]
 [-RemoveExplicitAccessRules] [<CommonParameters>]
```

## DESCRIPTION

Enables NTFS Access Control List inheritance on the directory specified in the Path parameter.

## EXAMPLES

### Example 1

```PowerShell
PS C:\> Enable-NTFSAccessInheritance -path t:\this\folder\is\disabled
```

Enables NTFS access control list inheritance on the directory "disabled"

### Example 2

```PowerShell
PS C:\> Enable-NTFSAccessInheritance -path t:\this\folder\is\disabled -RemoveExplicitAccessRules
```
Enables NTFS access control list inheritance on the directory "disabled" and removes the explicit access control entries in favor of the now inherited entries.  Note, this will remove the explicit access control entries even if they don't match the incoming inherited entries.

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

Path of directory to enable NTFS access control list inheritance.

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

### -RemoveExplicitAccessRules

Removes any existing explicit access control entries.

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
