**vnet**: logically isolated network within Azure that enables secure communication between Azure resources and with on-premises networks


**subnet**: A subnet is a segmented, smaller network within a VNet, used to organize and control the flow of traffic between Azure resources.

**storage account name must be unique globally**
storage types under storage account 
```bash
1.Blob: Designed for storing large amounts of unstructured data like text, images, videos, and backups
2.File:It is used to store files that need to be shared across multiple systems, just like a traditional file system. It supports the SMB protocol.
3.Table: designed for storing large amounts of structured data in the form of key-value pairs.
4. queue: Used for storing messages that help different parts of an application communicate and work independently.
```
```bash
ZRS------- It replicates your data across multiple availability zones within a region.
LRS ------ Data is replicated within a single region across multiple fault domains (usually 3 copies).
GRS------ It replicates your data to a secondary region for disaster recovery, ensuring data durability in case of regional outages.
RA-GRS----This can be useful if you need to access your data even during regional outages but don't need to write to it.
```


