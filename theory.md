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

```bash
Hot: Frequently accessed data(first 30 days)

cool storage:  It is for infrequently accessed data needing storage for at least 30 days ##(Hot to Cool Storage: Move blobs to cool after 30 days of last modification)

cold storage:  data that is for rarely accessed  that needs fast retrieval ## (For very infrequently accessed data with long-term retention ( 90 days)

Archive storage:  data that is rarely accessed and can tolerate very long access times ##(180 days )

Delete blobs after 2,555 days (approximately 7 years) of last modification
```
## Template format
```bash
<img width="458" alt="image" src="https://github.com/user-attachments/assets/e97718a9-f93d-4c9b-a92d-68eb436891e6" />



$schema	Yes ##  (used for validating deployment templates in Azure.) 
contentVersion	Yes ## (Version of the template)

resources	Yes
```

