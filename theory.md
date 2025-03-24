vnet: large portion of network


subnet: smaller portions of vnet


storage account name has be unique across world



ZRS------- It replicates your data across multiple availability zones within a region.

LRS ------ Data is replicated within a single region across multiple fault domains (usually 3 copies).
GRS------ It replicates your data to a secondary region for disaster recovery, ensuring data durability in case of regional outages.

RA-GRS----This can be useful if you need to access your data even during regional outages but don't need to write to it.


storage types under storage account 


blob
file
table
queue
