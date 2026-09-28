# 🧪 Experiment 8: Steganography Detection using StegExpose

**Aim:**  
To detect hidden data in image files using **StegExpose**, a steganalysis tool that identifies potential steganography based on statistical patterns.  

---

## 📝 Procedure  

### Step 1: Prepare Environment  
- Install **Java Runtime Environment (JRE)** on your system.  
- Verify installation using the command:  
  `java -version`  
- Download the **StegExpose.jar** tool from GitHub.  
- Place the `.jar` file and sample images in a working folder.  

---

### Step 2: Verify Dataset  
- Prepare a folder with mixed images:  
  - `clean_*.png` → Normal images without hidden data.  
  - `stego_*.png` → Images with embedded hidden data for testing.  
- Example folder path:  
  `C:\Users\krthc\Downloads\StegExpose-master\StegExpose-master\testFolder`

---

### Step 3: Run StegExpose  
- Open **PowerShell** or **Command Prompt** in the folder containing `StegExpose.jar`.  
- Execute the tool to analyze all images in the folder:  
  `java -jar StegExpose.jar "C:\Users\krthc\Downloads\StegExpose-master\StegExpose-master\testFolder"`

---

### Step 4: Generate Results  
- To export results to text and CSV format, run the following commands:  
  `java -jar StegExpose.jar ".\testFolder" default default "results_full.csv"`  
  `java -jar StegExpose.jar ".\testFolder" > results_full.txt`  
  `notepad results_full.txt`  

- The results file lists all analyzed images with their suspicion score and estimated hidden data size.  

---

### Step 5: Analyze Output  
- StegExpose flags suspicious images and estimates how much data is hidden.  
- The following output was generated in PowerShell after executing the command:  


`PS C:\Users\krthc\Downloads\StegExpose-master\StegExpose-master> java -jar StegExpose.jar "C:\Users\krthc\Downloads\StegExpose-master\StegExpose-master\testFolder"`
`stego_6666458261_e455d262b5_z.png is suspicious. Approximate amount of hidden data is 114785 bytes.`
`stego_6672108499_85c582a7f9.png is suspicious. Approximate amount of hidden data is 137047 bytes.`
`stego_6672542201_532f70bffe.png is suspicious. Approximate amount of hidden data is 67141 bytes.`

---

## ✅ Conclusion  
- Successfully identified hidden data in suspicious images using **StegExpose**.  
- Confirmed detection accuracy across multiple image types.  
- Results showed three images contained steganographic data, while others were clean.  

---
