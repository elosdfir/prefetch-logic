# **Prefetch Tools - Logic Overview**

---

## **TypeBypassHashes**

### **Explanation**
The command below clones the data from `File1.pf` into `File2.pf`. **TypeBypassHashes** scans every prefetch file on your computer to detect any two files that share the same hash. If a match is found, the tool will flag it.

### **Command**
```bash
Type [File1.pf] > [File2.pf]
```

---

## **TypeBypassEditTimes**

### **Explanation**
The command below clones the data from `File1.pf` into `File2.pf`. **TypeBypassEditTimes** scans every prefetch file on your computer and adds it to a CSV file using [WinPrefetchView](https://www.nirsoft.net/utils/winprefetchview-x64.zip). It then checks if the "Last Run Time" is ahead of or behind the "Modification Time" of the prefetch file by 60 or more seconds.

### **Command**
```bash
Type [File1.pf] > [File2.pf]
```

---

## **EXEDetectionByDLLImports**

### **Explanation**
After using [PECmd](https://download.ericzimmermanstools.com/net6/PECmd.zip) on a prefetch file to identify the common DLL imports made by a program, you can add those DLLs to the script. Running [PECmd](https://download.ericzimmermanstools.com/net6/PECmd.zip) again, the tool scans your entire prefetch folder. If it finds a file containing all the specified DLL imports, it displays the name of the prefetch file and its last run time.

---

# **Disclaimers**

- **TypeBypassHashes Disclaimer**  
  This tool cannot produce false flags. If it flags two files for having the same hash, it is definitively a cheat, as two `.pf` files cannot share the same hash. If you suspect a false flag, manually verify using the `.csv` file created by [PECmd](https://download.ericzimmermanstools.com/net6/PECmd.zip) to confirm the hash match.

- **TypeBypassEditTimes Disclaimer**  
  This tool can sometimes produce false flags. If you believe a file is falsely flagged, you can verify it in the CSV or directly in [WinPrefetchView](https://www.nirsoft.net/utils/winprefetchview-x64.zip).

- **EXEDetectionByDLLImports Disclaimer**  
  This tool will rarely produce false flags, provided you include multiple common DLL imports of the program you are checking.

---

<p align="center">
  <strong>Credits to <a href="https://discordapp.com/users/chrsx13"> @chrsx13</a> on Discord</strong>
</p>

