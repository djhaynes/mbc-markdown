|||
|---|---|
|**ID**|**E1014**|
|**Objective(s)**|[Defense Evasion](../defense-evasion)|
|**Related ATT&CK Technique**|[Rootkit](https://attack.mitre.org/techniques/T1014)|


Rootkit
=======
Behaviors of a rootkit: "A rootkit is a collection of computer software, typically malicious, designed to enable access to a computer or areas of its software that is not otherwise allowed and often masks its existence or the existence of other software." [[1]](#1)

See ATT&CK: [**Rootkit**](https://attack.mitre.org/techniques/T1014).

Rootkits may hide artifacts (kernel modules, services, threads, userspace libraries), prevent actions (API unhooking (prevents API hooks installed by the malware instance from being removed), file access (prevents access to the file system, including specific files and/or directories associated with the malware instance), file deletion (prevents files and/or directories associated with the malware instance from being deleted), memory access (prevents access to system memory where the malware instance stores code or data), native API hooking (prevents other software from hooking native system APIs), registry access (prevents access to the Windows registry, either entire registry or particular registry keys/values), registry deletion (prevents deletion of registry keys and/or values associated with the malware instance).

Methods
------- 
|Name|ID|Description|
|---|---|---|
|**Application Rootkit**|E1014.m12|Application rootkits operate by exchanging standard application files with rootkit files, or changing applications by injecting code or patching.|
|**Bootloader**|E1014.m13|A bootloader rootkit modifies the bootloader, enabling activation before the operating system is started. Also known as a Bootkit. See ATT&CK: [Bootkit](https://attack.mitre.org/techniques/T1542/003/).|
|**Hardware/Firmware Rootkit**|E1014.m14|A firmware rootkit compromises hardware (e.g. network card, hard drive), system BIOS, UEFI firmware. LoJack is the first in-the-wild UEFI rootkit. See ATT&CK: [System Firmware](https://attack.mitre.org/techniques/T1542/001/).|
|**Hypervisor/Virtualized Rootkit**|E1014.m15|A hypervisor (virtualized) rootkit hosts the target operating system as a virtual machine, enabling interception of all hardware calls. Also called, virtual-machine-based rootkit (VMBR).|
|**Kernel Mode Rootkit**|E1014.m16|Rootkit operates by adding or replacing code in OS, device drivers, loadable kernel modules (LKM). Related to ATT&CK: [Kernel Modules and Extensions](https://attack.mitre.org/techniques/T1547/006/)|
|**Memory Rootkit**|E1014.m17|A memory rootkit hids in RAM. Behaviors may include methods to prevent memory access. The lifespan of a memory rootkit is short because it disappears after a system reboot.|

Malware Examples
----------------
|Name|Date|Description|
|---|---|---|
|[**Poison-Ivy**](../xample-malware/poison-ivy.md)|2005|After the Poison-Ivy server is running on the target machine, the attacker can use a Windows GUI client to control the target computer. [[2]](#2)|

Detection
---------
Rootkits can be detected by detecting primary rootkit behaviors: Hide Artifacts, Impair Defenses, Highjack Execution Flow. Hidden artifacts include kernel modules (hides use of kernel modules used by the malware instance), services (hides any system services that the malware instance creates or injects itself into), threads (hides one or more threads that belong to the malware instance), userspace libraries (hides use of userspace libraries used by the malware instance). 

Rootkits can also be detected via memory dump analysis or virtual machine introspection.

References
----------
<a name="1">[1]</a> https://en.wikipedia.org/wiki/Rootkit

<a name="2">[2]</a> https://www.cyber.nj.gov/threat-profiles/trojan-variants/poison-ivy
