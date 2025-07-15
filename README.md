

# 1.Basic commend for new users  

## Cat : 

**open the any folder use *Cat* -> display the content of text file and concatenate several file to one file** 


```
- 1. View File Content :  `cat filename.txt`
```


```
- 2. View Multiple Files Together : `cat file1.txt file2.txt`
```

```
- 3. Create a New File : cat > newfile.txt ->  
```

```
4. Append to a File : **cat >> existingfile.txt
```


```
5. Redirect Output to Another File**

bash

`cat file1.txt > newfile.txt`
```


```
### 🔹 **6. Combine Files into One**

`cat file1.txt file2.txt > combined.txt`

```

```
Create two files with some content:

`echo "Hello from File 1" > file1.txt echo "Hello from File 2" > file2.txt`
```

## ✅ `ls -lah` — What Does It Do?

### 🔹 **Command Breakdown:**


`ls -lah`

|Option|Meaning|
|---|---|
|`-l`|Long format (detailed list: permissions, owner, size, date, etc.)|
|`-a`|All files, including hidden (`.` dot files)|
|`-h`|Human-readable file sizes (KB, MB, GB)|

---

## 🟦 **1. `ls` – List Directory Contents**

### ✅ Basic Usage:

```bash
ls
```

Lists files in the current directory.

---

### 🔧 Common Options:

|Command|What It Does|
|---|---|
|`ls -l`|Long listing format (permissions, size, owner, etc.)|
|`ls -a`|Show **all files**, including hidden ones (`.file`)|
|`ls -h`|Human-readable file sizes (use with `-l`)|
|`ls -la`|Long list + all files|
|`ls -lah`|Long list + all files + human-readable (💯 most useful)|
|`ls dir_name`|List files in a specific directory|

---

### 🧪 Example:

```bash
ls -lah /home/shafin
```

---

## 🟩 **2. `mkdir` – Make Directories**

### ✅ Basic Usage:

```bash
mkdir myfolder
```

---

### 🔧 Options:

| Command                 | What It Does                                                      |
| ----------------------- | ----------------------------------------------------------------- |
| `mkdir newfolder`       | Create a folder named `newfolder`                                 |
| `mkdir folder1 folder2` | Create multiple folders                                           |
| ***`mkdir -p a/b/c`***    | ***Create parent directories if they don’t exist (`a`, `b`, `c`)*** |

---

### 🧪 Example:

```bash
mkdir -p project/src/assets
```

---

## 🟨 **3. `cd` – Change Directory**

### ✅ Basic Usage:

```bash
cd foldername
```

Moves into a directory.

---

### 📁 Navigation Examples:

|Command|Meaning|
|---|---|
|`cd ..`|Go back one directory|
|`cd /`|Go to root directory|
|`cd ~`|Go to home directory|
|`cd -`|Go back to previous directory|
|`cd /home/shafin/Desktop`|Absolute path|
|`cd ../Documents`|Relative path|

---

### 🧪 Example:

```bash
cd /var/log
```

---

## 🟥 **4. `find` – Search for Files and Directories**

### ✅ Basic Syntax:

```bash
find [path] [options]
```

---

### 🔧 Common Use Cases:

|Command|Meaning|
|---|---|
|`find . -name "file.txt"`|Find file named `file.txt` in current and subdirectories|
|`find / -type d -name "config"`|Find directories named `config`|
|`find /home -type f -size +10M`|Find files larger than 10MB|
|`find . -name "*.sh"`|Find all `.sh` files|
|`find . -mtime -1`|Files modified **in the last 1 day**|
|`find . -empty`|Find **empty files/folders**|
|`find / -user shafin`|Find files owned by `shafin`|
|`find . -exec rm {} \;`|Run a command (like delete) on each match|

---

### 🧪 Practice:

```bash
find /etc -name "hosts"
find . -type f -name "*.log"
```

---

## ✅ Summary Table

|Command|Use|
|---|---|
|`ls`|List directory contents|
|`mkdir`|Create directories|
|`cd`|Navigate directories|
|`find`|Search files/directories by name, size, type, etc.|

---

## 📺 Recommended YouTube Videos (for Visual Learning)

| Topic                      | Channel            | Link                                                                                        |
| -------------------------- | ------------------ | ------------------------------------------------------------------------------------------- |
| `ls`, `mkdir`, `cd` basics | **NetworkChuck**   | [Linux CLI Crash Course](https://www.youtube.com/watch?v=ivlCv2Scrsk)                       |
| `find` command deep dive   | **DorianDotSlash** | [Linux `find` command tutorial](https://www.youtube.com/watch?v=4RPtJ9UyHS0)                |
| Linux CLI practice         | **The Net Ninja**  | [Linux Tutorials](https://www.youtube.com/playlist?list=PL4cUxeGkcC9jLYyp2Aoh6hcWuxFDX6PBJ) |

---

### 🔹 4. **Open Any File (Based on Its Type)**


`xdg-open filename`

`This will open the file in the default application (like double-clicking in GUI).`

`Example:`

`xdg-open myphoto.jpg`

| Action                    | Command                             |
| ------------------------- | ----------------------------------- |
| View file                 | `cat file.txt` or `less file.txt`   |
| ==Edit file (easy)==      | ==`nano file.txt`==                 |
| Edit file (advanced)      | `vim file.txt`                      |
| GUI text editor           | `gedit file.txt` or `kate file.txt` |
| ==Open with default app== | ==`xdg-open file`==                 |
| Run Python file           | `python3 file.py`                   |
## 1️⃣ Move Files or Directories

### Syntax:

`mv source_path destination_path`

### Examples:

- Move a file:

`mv file.txt /home/user/Documents/`

- Move and rename a file at the same time:
    
`mv oldname.txt newname.txt`

- Move a directory:

`mv myfolder /home/user/Desktop/`

---

## 2️⃣ Delete Files or Directories

### Delete a file:

`rm filename.txt`

### Delete an empty directory:

`rmdir directoryname`

### Delete a directory and all its contents (use with care!):

`rm -r directoryname`

- `-r` means recursive (delete directory and everything inside)
    

---

## 3️⃣ Rename Files or Directories

**Renaming is done with `mv` command**, just move the file/directory to the same location but with a new name:

`mv oldname.txt newname.txt`

`mv oldfoldername newfoldername`

---

## Summary Table

| Action                 | Command Example                     |
| ---------------------- | ----------------------------------- |
| Move file              | `mv file.txt /path/to/destination/` |
| Rename file            | `mv oldname.txt newname.txt`        |
| Delete file            | `rm file.txt`                       |
| Delete empty dir       | `rmdir myfolder`                    |
| Delete dir recursively | `rm -r myfolder`                    |

---

**Be careful with `rm -r`**, especially as root (`sudo`), because deleted files usually can’t be recovered.
### Important tips:

- This **permanently deletes** the file (no recycle bin).
    
- To avoid accidental deletion, you can use the interactive option:
    
`rm -i example.txt`