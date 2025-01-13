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



