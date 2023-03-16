## Restart to bios:
```
shutdown /r /fw /f /t 0
```
## Get a battery report:
``` 
powercfg /batteryreport
```
## Checking the disk health:
``` 
chkdsk /f
chkdsk /r
```
## Running windows system file checker tool:
``` 
sfc /scannow
```
## Repair corrupted files online using windows deployment: image servicing and management:
```sh
DISM /Online /Cleanup-Image /{x}
```
- CheckHealth only checking the health
- ScanHealth to check in more depth" 
- RestoreHealth restore health
## Killing a task:
```sh
taskkill /f /pid "programName"
```

---
#shell #command_line #bash
