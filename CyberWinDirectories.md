Simple Cyber Security about Windows Directories
## Credential and Access Logs
Stores local password hashes (target for credential dumping attacks).
```
C:\Windows\System32\config\SAM
```
Backup of user credentials (potential target for attackers). 
```
C:\Windows\repaire\SAM
```
Holds security policies and access control settings.
```
C:\Windows\System32\config\SECURITY
```
## System and Event Logs
Stores Windows Event Logs (Crucial for SIEM correlation).
```
C:\Windows\System32\winevt
```
Tracks system-wide changes and configurations
```
C:\Windows\System32\config\SYSTEM
```
Registry hive with details on installed software and changes
```
C:\Windows\System32\config\SOFTWARE
```
## Malware and Threat Hunting Indicators
Tracks recently executed programs (userful for forensic timelines).
```
C:\Windows\Prefetch
```
Logs details of executed applications, great for detecting lateral movement.
```
C:\Windows\AppCompat\Programs\Amcache.hve
```
Holds user-specific registry settings, often abused for persistence.
```
C:\Users\*\NTUSER.dat
```
Persistence and Startup Investigations
User-specific persistence mechanisms.
```
C:\Users\*\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup
```
Global startup folder for all users (Often misused by malware).
```
C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startuo
```
