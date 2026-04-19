# 💾 Windows Backup & Recovery Lab

## 📌 Overview
This project demonstrates how to perform a full Windows system backup using built-in tools and verify the integrity of the backup. It focuses on system image creation, recovery readiness, and command-line usage.

---

## 🎯 Objective
- Create a full system backup using wbAdmin  
- Understand how Windows handles system image backups  
- Verify backup contents and structure  

---

## 🖥️ Environment
- Device: Dell Inspiron 5505  
- OS: Windows 11 Pro  
- Tools: wbAdmin, External Backup Drive  

---

## ⚙️ Process
1. Connected external backup drive  
2. Configured storage partitions  
3. Executed system backup using wbAdmin  
4. Verified backup contents and logs  

---

## 🧪 Commands Used

- Start full system backup:

```
wbadmin start backup -backupTarget:B: -include:C: -allCritical -quiet
```

- View available backup versions:

```
wbadmin get versions
```

- Inspect backup contents (use a timestamp from `wbadmin get versions`):

```
wbadmin get items -version:<timestamp>
```

## 📊 Results
- Full system image successfully created  
- Critical partitions included (EFI, Recovery, OS)  
- Backup verified through wbAdmin commands  

---

## 🐛 Issues Encountered
- Understanding backup structure and partition inclusion  
- Interpreting wbAdmin output  

---

## 🔧 Resolution
- Reviewed backup logs and verified included volumes  
- Confirmed system state and critical volumes were included  

---

## 💡 Key Takeaways
- wbAdmin is a powerful built-in backup tool  
- Full system backups include more than just the OS partition  
- Verifying backups is as important as creating them  

---

## 🚀 Future Improvements
- Test full system recovery process  
- Automate backups with scheduled tasks  
- Compare with third-party backup tools  

