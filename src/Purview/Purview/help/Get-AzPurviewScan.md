---
external help file:
Module Name: Az.Purview
online version: https://docs.microsoft.com/powershell/module/az.purview/get-azpurviewscan
schema: 2.0.0
---

# Get-AzPurviewScan

## SYNOPSIS
Gets a scan information

## SYNTAX

### List (Default)
```
Get-AzPurviewScan -Endpoint <String> -DataSourceName <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Get
```
Get-AzPurviewScan -Endpoint <String> -DataSourceName <String> -Name <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzPurviewScan -Endpoint <String> -InputObject <IPurviewdataIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## DESCRIPTION
Gets a scan information

## EXAMPLES

### Example 1: Get scan instance within a data source
```powershell
PS C:\> Get-AzPurviewScan -Endpoint 'https://parv-brs-2.purview.azure.com/' -DataSourceName 'DataScanTestData-Parv' -Name 'ScanTest'

CollectionLastModifiedAt  : 2/15/2022 3:49:23 PM
CollectionReferenceName   : parv-brs-2
CollectionType            : CollectionReference
ConnectedViaReferenceName :
CreatedAt                 : 2/15/2022 3:49:23 PM
CredentialReferenceName   : datascantestdataparv-accountkey
CredentialType            : AccountKey
Id                        : datasources/DataScanTestData-Parv/scans/ScanTest
Kind                      : AzureStorageCredential
LastModifiedAt            : 2/15/2022 11:46:29 PM
Name                      : ScanTest
Result                    :
ScanRulesetName           : AzureStorage
ScanRulesetType           : System
Worker                    :
```

Get scan instance named 'ScanTest' within a data source

### Example 2: Get all scan instances within a data source
```powershell
PS C:\>  Get-AzPurviewScan -Endpoint 'https://parv-brs-2.purview.azure.com/' -DataSourceName 'DataScanTestData-Parv'

CollectionLastModifiedAt  : 2/13/2022 3:16:24 PM
CollectionReferenceName   : parv-brs-2
CollectionType            : CollectionReference
ConnectedViaReferenceName :
CreatedAt                 : 2/13/2022 3:16:24 PM
CredentialReferenceName   : datascantestdataparv-accountkey
CredentialType            : AccountKey
Id                        : datasources/DataScanTestData-Parv/scans/Scan1ForDemo
Kind                      : AzureStorageCredential
LastModifiedAt            : 2/13/2022 3:16:24 PM
Name                      : Scan1ForDemo
Result                    :
ScanRulesetName           : AzureStorage
ScanRulesetType           : System
Worker                    :

CollectionLastModifiedAt  : 2/15/2022 3:49:23 PM
CollectionReferenceName   : parv-brs-2
CollectionType            : CollectionReference
ConnectedViaReferenceName :
CreatedAt                 : 2/15/2022 3:49:23 PM
CredentialReferenceName   : datascantestdataparv-accountkey
CredentialType            : AccountKey
Id                        : datasources/DataScanTestData-Parv/scans/ScanTest
Kind                      : AzureStorageCredential
LastModifiedAt            : 2/15/2022 11:46:29 PM
Name                      : ScanTest
Result                    :
ScanRulesetName           : AzureStorage
ScanRulesetType           : System
Worker                    :
```

Get all scan instances within a data source

## PARAMETERS

### -DataSourceName
.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpoint
The scanning endpoint of your purview account.
Example: https://{accountName}.purview.azure.com

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter
To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Purview.Models.IPurviewdataIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ScanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Purview.Models.IPurviewdataIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Purview.Models.Api20211001Preview.IScan

## NOTES

ALIASES

COMPLEX PARAMETER PROPERTIES

To create the parameters described below, construct a hash table containing the appropriate properties. For information on hash tables, run Get-Help about_Hash_Tables.


INPUTOBJECT <IPurviewdataIdentity>: Identity Parameter
  - `[ClassificationRuleName <String>]`: 
  - `[ClassificationRuleVersion <Int32?>]`: 
  - `[DataSourceName <String>]`: 
  - `[DataSourceType <DataSourceType?>]`: 
  - `[Id <String>]`: Resource identity path
  - `[KeyVaultName <String>]`: 
  - `[RunId <String>]`: 
  - `[ScanName <String>]`: 
  - `[ScanRulesetName <String>]`: 
  - `[Version <Int32?>]`: 

## RELATED LINKS

