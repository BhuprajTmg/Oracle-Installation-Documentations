# SQL Server Configuration

## SSMS Verification
After installation:
- Verify version/build number  
- Review Server Properties  

## Memory Settings
- Max Server Memory: **85%** of total RAM  
- Min Server Memory: **4096 MB**  

## Security Settings
- Authentication: **Mixed Mode**  
- Login auditing: Failed logins only  

## Connection Settings
- Allow remote connections  
- Remote query timeout: **600**  

## Database Settings
- Default index fill factor: **0**  
- Enable: **Compress Backup**  
- Verify default data/log directories  
- Set default backup directory  

## Advanced Settings
- Optimize for Ad hoc Workloads: **True**  
- Cost Threshold for Parallelism: **100**  
- Max Degree of Parallelism:  
  - Half of available cores  
  - Max value: 8  

## System Databases
For master, model, msdb:
- Recovery model: **Simple**  
- Autogrowth: **Fixed increments**  

## SQL Server Logs
- Limit number of error logs: **99**  

## SQL Server Agent
- Auto‑restart enabled  
- Max job history rows per job: **100**  
- Max job history log size: **10000**  

## Server Name Verification
Run:

SELECT HOST_NAME() AS 'host_name()',
@@servername AS 'ServerName\InstanceName',
SERVERPROPERTY('servername') AS 'ServerName',
SERVERPROPERTY('machinename') AS 'Windows_Name',
SERVERPROPERTY('ComputerNamePhysicalNetBIOS') AS 'NetBIOS_Name',
SERVERPROPERTY('instanceName') AS 'InstanceName',
SERVERPROPERTY('IsClustered') AS 'IsClustered';

If mismatch:
EXEC sp_DROPSERVER 'oldservername';
EXEC sp_ADDSERVER 'newservername', 'local';

Restart SQL Services.