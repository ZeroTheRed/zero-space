**Persistent Partition** - If you have any files that you wish to persist or remain after reboot/installing the OS, then a persistent partition is required. This is the space that will remain unchanged and data to be preserved can be put in here

**Partition Scheme**

| **MBR**                                                      | **GPT**                                    |
| ------------------------------------------------------------ | ------------------------------------------ |
| Older boot record filesystem but greater compatibility       | Newer but less compatible                  |
| Required for booting with BIOS or FAT filesystems            | Required for booting with UEFI filesystems |
| Max 4 primary partitions or 3 primary + 1 extended partition | Supports $\infty$ partitions               |
If you're using BIOS, set MBR
If you're using UEFI, set GPT

**Target System** - The target system will be either _BIOS or UEFI (CSM)_ if you have chosen MBR and _UEFI (non-CSM)_ if GPT is chosen
	**CSM** - Compatibility Support Module. Most UEFI systems have this module to support legacy BIOS booting

**Cluster Size** - Each drive has a default cluster size. It's recommended to leave it at the defaults unless you know what you're doing 