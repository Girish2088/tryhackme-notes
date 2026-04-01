

##  Common Commands

###  File & Directory Management
- `Get-ChildItem` → List files and directories  
- `Set-Location` → Change directory  
- `Get-Content` → Read file content  
- `Set-Content` → Write/overwrite file  
- `Copy-Item` → Copy files  
- `Move-Item` → Move or rename files  
- `Remove-Item` → Delete files  

---

###  Process & System Commands
- `Get-Process` → View running processes  
- `Get-Service` → Check system services  
- `Get-NetTCPConnection` → View network connections  

---

###  Security
- `Get-FileHash` → Generate file hash (integrity check)  



## 🔄 Data Processing (Core Power)

# Filtering
- `Where-Object`
- Get-ChildItem | Where-Object Length -gt 100

# Searching Text
- `Select-String`
- Select-String -Path file.txt -Pattern password


# Sorting
- `Sort-Object`
- Get-ChildItem | Sort-Object Length


# Selecting Specific Data
- `Select-Object`
-Get-ChildItem | Select-Object Name, Length
---

#Selecting Specific Data
- `Select-Object`
- Get-ChildItem | Select-Object Name, Length

 
---

## 🔗 Power of Pipeline

PowerShell allows chaining commands:

Get-Thing | Where-Object condition | Sort-Object property | Select-Object needed


Example:
Get-Process | Where-Object CPU -gt 50 | Sort-Object CPU -Descending | Select-Object -First 3



---

## Windows vs Linux vs PowerShell

| Task            | PowerShell        | Windows CMD | Linux |
|-----------------|------------------|-------------|-------|
| List files      | Get-ChildItem    | dir         | ls    |
| Change dir      | Set-Location     | cd          | cd    |
| Read file       | Get-Content      | type        | cat   |
| Copy file       | Copy-Item        | copy        | cp    |
| Delete file     | Remove-Item      | del         | rm    |
| Processes       | Get-Process      | tasklist    | ps    |

---

# What I Practiced
- Navigating directories using PowerShell
- Managing files (create, read, copy, delete)
- Filtering and searching data using pipelines
- Monitoring processes and network connections


---

## 🚧 Improvements / Next Steps
- Learn PowerShell scripting basics (.ps1 files)
- Practice automation tasks using scripts
- Explore advanced filtering and object properties
