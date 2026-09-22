# NETWORKWALKS-B083-WK3-CYBERSECURITY-PASSWORD-CRACKING-WITH-JTR-
Password Cracking with JTR

| Field | Details |
| :--- | :--- |
| Crscker's Name | Alfred Owino |
| Program / Batch | B083 - Networkwalks Cybersecurity Internship.|
| Date | 23 September 2026. |
| Modules Completed | W3-PM1 (Password Cracking with JTR)|
| Client / Target | Networkwalks encrypted PDF document.|
| Permission Secured? | Yes (Assignment) |
| Phases Covered | Phase 1: Hash Extraction<br> Phase 2:Attack /Execution<br>Phase 3: Password Recovery 


 OBJECTIVES
Primary Objective: Successfully recover known and unknown passwords protecting three separate target PDF files and extract the embedded confirmation flags
Operating System: Windows host environment / Security lab utility suite.

TOOLS USED
Johnny / John the Ripper:** Password cracking framework used for hash identification and dictionary/brute-force execution.
PDF Reader: For validating successful decryption and viewing flag artifacts.

 METHODOLOGY.
 
a. Hash Identification and Extraction
When dealing with password-protected PDF files, modern security tools cannot attack the document directly through raw plaintext guesses at scale. Instead, Hash Identification and Extraction is used which involves:

 Inspecting the target PDF to evaluate its encryption standard
 Extracting the internal document hash format compatible with offline cracking tools.

 b. Attack Execution
Using Johnny, the extracted hashes were loaded into the workspace interface and an attack was launched on it which cracked the password

 RESULT

| Target File | Recovered Password | Status |
| :--- | :--- | :--- |
| PDF Target 1 | `good-luck`| Cracked |
| PDF Target 2 | `password1`| Cracked |
| PDF Target 3 | `1qaz2wsx` | Cracked |

Upon successful recovery, each password was used to decrypt its respective PDF file, revealing the confirmation in the encrypted file.

KEY SECURITY TAKEAWAY

Weak Passwords:  Passwords such as `password1` or simple predictable strings are vulnerable to rapid dictionary and wordlist-based offline attacks.

Encryption Strength: Even when strong underlying encryption standards, overall file security is entirely dependent on the entropy and length of the user-chosen password.

Defense-in-Depth: Organizations should enforce strict password complexity policies, implement multi-factor access controls, and avoid sharing sensitive documents protected by easily guessable credentials.



 LIABITITY DISCLAIMER!
The tools, techniques, and methodologies detailed in this repository are intended for educational purposes, authorized security testing, and completion of coursework for the Networkwalks Cybersecurity program. The author assumes no liability for the misuse of this information.*
  
