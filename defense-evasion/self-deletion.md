|||
|---|---|
|**ID**|**F0007**|
|**Objective(s)**|[Defense Evasion](../defense-evasion)|
|**Related ATT&CK Sub-Technique**|[Indicator Removal on Host: Uninstall Malicious Application](https://attack.mitre.org/techniques/T1630/001/), [Indicator Removal on Host: File Deletion](https://attack.mitre.org/techniques/T1070/004/)|


Self Deletion
=============
Malware may uninstall itself to avoid detection. 

See ATT&CK: [**Indicator Removal on Host: Uninstall Malicious Application**](https://attack.mitre.org/techniques/T1630/001/), [**Indicator Removal on Host: File Deletion**](https://attack.mitre.org/techniques/T1070/004/).

Methods
-------
|Name|ID|Description|
|---|---|---|
|**COMSPEC Environment Variable**|F0007.001|Uninstalls self via COMSPEC environment variable.|
