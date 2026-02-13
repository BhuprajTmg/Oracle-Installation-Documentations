# Minimum Configuration (Per Instance)

> Note: It is not recommended to install multiple instances in non‑clustered production servers without sufficient resources.

## Hardware Requirements
- 4 CPU cores  
- 64 GB RAM  

## Drive Configuration (RAID5 minimum)
- **C:** 150GB — Windows OS only  
- **D:** 150GB — Applications  
- **F:** 250GB+ — Database MDF files  
- **L:** 250GB+ — Database LDF files  
- **T:** 250GB+ — TempDB files  
- **U:** 250GB+ — TempDB log file  
- **S:** 100GB+ — System databases  

Additional drives may be required for high growth or IOPS workloads.

## AWS EBS Recommendation
- Volume Type: gp3  
- Throughput: 125  
- IOPS: 3000  

## Renaming Drives
1. Open Disk Management → Change Drive Letter  
2. Open CMD as Administrator  
3. Example:
