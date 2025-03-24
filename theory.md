**vnet**: logically isolated network within Azure that enables secure communication between Azure resources and with on-premises networks


**subnet**: A subnet is a segmented, smaller network within a VNet, used to organize and control the flow of traffic between Azure resources.

**storage account name must be unique globally**
storage types under storage account 
1.blob
2.file
3.table
4. queue

```bash
ZRS------- It replicates your data across multiple availability zones within a region.
LRS ------ Data is replicated within a single region across multiple fault domains (usually 3 copies).
GRS------ It replicates your data to a secondary region for disaster recovery, ensuring data durability in case of regional outages.
RA-GRS----This can be useful if you need to access your data even during regional outages but don't need to write to it.
```


