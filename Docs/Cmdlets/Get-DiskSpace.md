---
external help file: NTFSSecurity.dll-Help.xml
Module Name: ntfssecurity
online version:
schema: 2.0.0
---

# Get-DiskSpace

## SYNOPSIS

Gets drive size and space information

## SYNTAX

```
Get-DiskSpace [[-DriveLetter] <String[]>] [<CommonParameters>]
```

## DESCRIPTION

{{ Fill in the Description }}

## EXAMPLES

### Example 1

```PowerShell
PS C:\> Get-DiskSpace -DriveLetter c:

AvailableFreeSpacePercent  : 23.25%
AvailableFreeSpaceUnitSize : 55.23 GB
ClusterSize                : 4096
DriveName                  : c:\
TotalSizeUnitSize          : 237.53 GB
UsedSpacePercent           : 76.75%
UsedSpaceUnitSize          : 182.3 GB
FreeBytesAvailable         : 59301740544
TotalNumberOfBytes         : 255049330688
TotalNumberOfFreeBytes     : 59301740544
BytesPerSector             : 512
NumberOfFreeClusters       : 14477964
SectorsPerCluster          : 8
TotalNumberOfClusters      : 62267903
```

Get-Diskspace quickly returns various disk size and space values for the specified drive letter.

## PARAMETERS

### -DriveLetter

{{ Fill DriveLetter Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Alphaleonis.Win32.Filesystem.DiskSpaceInfo

## NOTES

## RELATED LINKS
