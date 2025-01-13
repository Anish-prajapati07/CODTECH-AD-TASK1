# CODTECH-AD-TASK1

Name:Anish Prajapati

Company:CODTECH IT SOLUTIONS

ID: CT08EDO

Domain:Cyber security and Ethical hacking

Duration:December 17th,2024 to january 17th,2025

Mentor:Neela Santhosh Kumar

# Overview
•	BUILD A TOOL TO MONITOR CHANGES IN FILES BY CALCULATING AND COMPARING HASH VALUES.

•A PYTHON SCRIPT USING LIBRARIES LIKE HASHLIB TO ENSURE FILE INTEGRITY.

# Main Features
1.	Hash-Based File Monitoring:
		
  •	Uses SHA-256 hashing to generate a unique fingerprint for each file.

  •	Hash values are stored in a JSON file (file_hashes.json) for comparison in subsequent runs.

2.	Change Detection:
    
  •	Compares the current state of files in the directory with the stored hash values.

  •	Detects:

   	Added files: New files that did not exist previously.
  
   	Modified files: Files whose content has changed.
  
   	Removed files: Files that no longer exist.


3.	Persistent State:

  •	Saves file hash data in a JSON file to maintain state across multiple script runs.

# How It Works

How It Works

1.	Initialization:

•	The FileIntegrityChecker class is initialized with:

   directory: The directory to monitor.

   hash_file: The JSON file where hash data is stored.

•	Existing hash data is loaded from the JSON file if it exists.

2.	File Hash Calculation:

•	The calculate_hash method computes a SHA-256 hash for each file, reading the file in chunks (8192 bytes) to handle large files efficiently.

4.	Directory Scanning:

•	The scan_files method recursively traverses the specified directory, calculating hash values for all files.

3.	Change Detection:

 •	The monitor_changes method compares the current file hashes with the stored hashes:
   
   	Added Files: Files present in the directory but not in the stored hashes.
   
   	Modified Files: Files with hash values that differ from the stored values.
   
   	Removed Files: Files listed in the stored hashes but missing from the directory.

4.	Updating State:

•	After detecting changes, the script updates the stored hash values and saves them to the JSON file for future comparisons.

# Limitations :

1.	No Real-Time Monitoring: The script requires manual execution to detect changes and cannot monitor files continuously in real time.

2.	Rename Detection: It cannot detect if a file was renamed, treating it as a removed file and a new addition.

3.	Metadata Ignorance: The script focuses only on file content (hash) and ignores changes in metadata like timestamps or permissions.

4.	Performance on Large Directories: Scanning large directories with many files may be slow due to recalculating hashes for every file.

5.	Hash File Corruption: If the JSON hash file gets corrupted, the stored file integrity data may be lost.

# OUTPUT

![image](https://github.com/user-attachments/assets/1be31e32-d7ec-40a4-9d67-b68b81fef2ea)











