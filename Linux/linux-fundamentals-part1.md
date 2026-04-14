# Linux Fundamentals Part 1 (Short Notes)

## 📂 Navigation
- `pwd` → Show current directory  
- `ls` → List files/folders  
- `cd <dir>` → Change directory  

---

## 📄 File Handling
- `cat <file>` → View file content  

---

## 🔍 File Search (find)
- Used to search **files by name**

Examples:
- `find -name file.txt` → Exact name  
- `find -name "*.txt"` → All .txt files  

### 📌 Scope
- `find .` → Search current directory  
- `find /` → Search entire system  

---

## 🔎 Text Search (grep)
- Used to search **inside files**

Examples:
- `grep "text" file.txt` → Search in file  
- `grep -R "text" .` → Search in directory  

---

## ⚡ Error Handling (Important)

### `2>/dev/null`

- `2` → Error output (stderr)  
- `>` → Redirect  
- `/dev/null` → Discard output  

👉 Used to **hide permission errors**

Example:
- `find / -name "*.txt" 2>/dev/null`

---

## ⚔️ find vs grep

### `find`
- Searches **file names**
- Use when you don’t know file location  

Example:
