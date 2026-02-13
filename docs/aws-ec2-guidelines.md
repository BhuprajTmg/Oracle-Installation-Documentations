# AWS EC2 SQL Server Guidelines

## Recommended Instance Type
- **r6i** family  
- Disk types: **io1 / io2**  

Instance size should be selected based on:
- Current CPU/memory usage  
- Performance requirements  
- Cost analysis  

## Drive Layout (EC2)
- **C:** 150GB — Windows OS  
- **E:** 150GB — Applications + SQL Server  
- **D:** 2× total current MDF size — Data files  
- **L:** 2× total current LDF size — Log files  
- **T:** 150GB — TempDB  
- **N:** As required — Backups, archived logs  

## Memory Allocation
- SQL Server should use **75%** of total memory if hosting only the DB engine  

## TempDB
- 1 file per CPU (up to 8)  
- Single TempDB log file  
