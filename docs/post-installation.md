# Post‑Installation Tasks

## High Availability
If the instance will join an Availability Group:
- Enable HADR in SQL Configuration Manager  
- Restart SQL Server  

## SSMS Validation
- Confirm version/build  
- Validate all server settings  

## SQL Agent
- Enable auto‑restart  
- Configure job history retention  

## System Database Configuration
- Set recovery model to **Simple**  
- Configure fixed autogrowth increments  

## Error Log Configuration
- Limit error logs to **99**  
