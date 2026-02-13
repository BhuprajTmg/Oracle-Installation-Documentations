# Uninstall & Reinstall SQL Server (AWS Preinstalled Version)

When AWS provides a preinstalled SQL Server instance without SA password, uninstall it.

## Uninstall Steps
1. Open **Add/Remove Programs**  
2. Select **Microsoft SQL Server 2019 (64-bit)** → Uninstall  
3. Remove:
   - SQL Server  
   - Microsoft OLE DB Driver  
   - ODBC Driver  
4. Restart server  

## Reinstall Steps
1. Run `setup.exe`  
2. Choose **New SQL Server stand‑alone installation**  
3. Product key is preloaded  
4. Accept license terms  
5. Select features (Database Engine only)  
6. Leave instance root directory default  
7. Configure service accounts  
8. Enable *Grant Volume Maintenance Task*  
9. Choose Mixed Mode  
10. Configure:
    - Data directory  
    - Log directory  
    - Backup directory  
    - TempDB (4 files)  
11. Install and reboot  
