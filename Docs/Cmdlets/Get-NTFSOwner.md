---
external help file: NTFSSecurity.dll-Help.xml
Module Name: ntfssecurity
online version:
schema: 2.0.0
---

# Get-NTFSOwner

## SYNOPSIS

Get-NTFSOwner returns the owner of a file or directory.

## SYNTAX

### Path (Default)
```
Get-NTFSOwner [[-Path] <String[]>] [<CommonParameters>]
```

### SecurityDescriptor
```
Get-NTFSOwner [-SecurityDescriptor] <FileSystemSecurity2[]> [<CommonParameters>]
```

## DESCRIPTION

{{ Fill in the Description }}

## EXAMPLES

### Example 1

```PowerShell
PS C:\>  Get-NTFSOwner T:\Administration\ | Format-List

Item     : T:\Administration\
Owner    : BUILTIN\Administrators
Account  : BUILTIN\Administrators
FullName : T:\Administration
```

Returns the owner of the Administration directory.

## PARAMETERS

### -Path

The path or paths to the file or directory to get the owner of.

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

### Security2.FileSystemOwner

## NOTES

## RELATED LINKS
