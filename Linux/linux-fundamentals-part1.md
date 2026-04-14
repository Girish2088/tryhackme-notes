# 🐧 Linux Fundamentals Part 1 (Quick Notes)

## 📂 Navigation
- `pwd` → Current directory  
- `ls` → List files/folders  
- `cd <dir>` → Change directory  

---

## 📄 File Handling
- `cat <file>` → View file content  

---

## 🔍 File Search (`find`)
- Searches **file names**

### Examples
- `find -name "file.txt"` → Exact file  
- `find -name "*.txt"` → All `.txt` files  

### Scope
- `find .` → Current directory  
- `find /` → Entire system  

---

## 🔎 Text Search (`grep`)
- Searches **inside files**

### Examples
- `grep "text" file.txt` → Search in file  
- `grep -R "text" .` → Search in directory  

---

## ⚡ Error Handling
### `2>/dev/null`
- `2` → Error output  
- `>` → Redirect  
- `/dev/null` → Discard output  

👉 Hides permission errors  

Example:
bash
find / -name "*.txt" 2>/dev/null



⚔️ find vs grep
find → File name search
find / -name "*tiger*" 2>/dev/null
grep → Content search
grep -R "tiger" /var/log 2>/dev/null
