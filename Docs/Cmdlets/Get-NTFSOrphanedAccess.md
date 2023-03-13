---
external help file: NTFSSecurity.dll-Help.xml
Module Name: ntfssecurity
online version:
schema: 2.0.0
---

# Get-NTFSOrphanedAccess

## SYNOPSIS

Returns Access Control entries for orphaned account objects.

## SYNTAX

### Path
```
Get-NTFSOrphanedAccess [[-Path] <String[]>] [-Account <IdentityReference2>] [-ExcludeExplicit]
 [-ExcludeInherited] [<CommonParameters>]
```

### SD
```
Get-NTFSOrphanedAccess [-SecurityDescriptor] <FileSystemSecurity2[]> [-Account <IdentityReference2>]
 [-ExcludeExplicit] [-ExcludeInherited] [<CommonParameters>]
```

## DESCRIPTION

{{ Fill in the Description }}

## EXAMPLES

### Example 1

```PowerShell
PS C:\>  Get-NTFSOrphanedAccess T:\Administration\ | format-list

Name               : Administration
FullName           : T:\Administration
InheritanceEnabled : False
InheritedFrom      :
AccessControlType  : Allow
AccessRights       : Modify, Synchronize
Account            : S-1-5-21-2139493591-2076723391-1105138716-23672
InheritanceFlags   : ContainerInherit, ObjectInherit
IsInherited        : False
PropagationFlags   : None
AccountType        :
```

One access control entry is returned for the orphaned account object.

### Example 2

```PowerShell
PS C:\>  Get-NTFSOrphanedAccess T:\Administration\ | remove-ntfsaccess 
```
Finds and removes access control entries for account objects that no longer exist in the domain.

## PARAMETERS

### -Account

{{ Fill Account Description }}

```yaml
Type: IdentityReference2
Parameter Sets: (All)
Aliases: IdentityReference, ID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeExplicit

When specified, explicit access control entries will be excluded from the results.

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

### -ExcludeInherited

When specified, inherited access control entries will be excluded from the results.

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

The path or paths to the directory or directories to get orphaned access control entries for.

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
Parameter Sets: SD
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

### Security2.IdentityReference2

## OUTPUTS

### Security2.FileSystemAccessRule2

## NOTES

## RELATED LINKS
