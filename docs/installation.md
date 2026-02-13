# SQL Server Installation

## Pre‑Installation Steps
1. Turn off Windows Defender Firewall for all networks.  
2. Edit the hosts file:  
   - Path: `C:\Windows\System32\drivers\etc\hosts`  
   - Add server IP and hostname  
   - Example:  
     ```
     10.16.20.206 austin
     ```
3. Mount the SQL Server installation image.  
4. Choose edition → Standalone installation.  
5. Ensure all installation rules pass.  
6. Select required features.  
7. Choose default or named instance.  

## Installation Location
- Installation directory: **D:**  
- Database files: **G:**  
- Log files: **L:**  

## TempDB Configuration (SQL 2016+)
- One TempDB file per CPU (up to 8)  
- All TempDB files must have:
  - Identical initial size  
  - Identical fixed autogrowth (not percentage)  
- Single TempDB log file  
- Max size must not exceed available drive space  

## Backup Configuration
- Set backup location to a separate drive (if available)  
- Uncheck: *Allow SQL Server to perform volume maintenance tasks*  

## Security
- Authentication Mode: **Mixed Mode**  
- Set SA password per corporate policy  
- Assign SQL SysAdmin role to required groups  

## Patching Order
- SQL 2017+: Latest CU  
- Below 2017:  
  1. Service Pack  
  2. Latest CU  
  3. Hotfix  
  4. Latest security update  

Reboot server as required.
