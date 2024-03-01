Blob 
Storage account - unique azure namepsace for your data. 
Blobs are stored in storage account in a container. 

Storage account -> Container -> Blob of data 

Blob types: 
- Block - store text an binary data up to 4.7TB . Made of individually managed blocks of data 
- Append - Block blobs that are optimized for append operations
- Page - store files up to 8TB. Any part of file could be accessed at any time  for example virtual hard drive 

Pricing tiers: 
- Hot 0 frequently accessed files - lower access times and higher costs 
- Cool - higher access time lower cost. Data remains at least 30 days 
- Archive - lowest cost and highest access times 


Disk  - disk to store data on 
- dont need  to worry about bak 
- managed by azure 
- flexibe, can change storage size 
- disk types : hdd, ssd, premium ssd and ultra disk 

File 
 - rsdilient, managed by azure, easy sharing 

Archive - lowest price, not very fast 

Storage Redundancy 
- automatic, invisible to user, min 3 copies of data 
- single zone, multiple zone or multiple regions
- higher availability - higher cost 


Options: 
- LRS - Locally redundant storage, lowest cost, protect against single disk failure, does not protect against zone or regional outage 
- ZRS - Zone-Redundant Storage , three copies of data, one in each availability zone, protect against zone outage but not regional outage
- GRS - Geo-Redundant Storage, three copies in primary regional physical location, three copies in secondary region
- GZRS 

Moving data and migration options 
AzCopy - command lin utiliity, able to transfer files and blobs, good for scripting 
Storage explorter - GUI tool , downloaded application 
Azure File Sync - works with azure files, sync with on premises file servers 

Premium performance options 