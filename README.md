# NETWORKWALKS-B083-WK3-CYBERSECURITY-PASSWORD-CRACKING-WITH-JTR-
Password Cracking with JTR

The primary focus of this assignment was to understand the cryptographic mechanisms protecting encrypted document formats (PDFs), identify hash structures, and execute offline brute-force and dictionary-based password cracking attacks using *John the Ripper* (via the *Johnny* graphical user interface)[span_1](start_span)[span_1](end_span)[span_2](start_span)[span_2](end_span)[span_3](start_span)[span_3](end_span). 

---

## Lab Environment & Objectives
* *Primary Objective:* Successfully recover known and unknown passwords protecting three separate target PDF files and extract the embedded confirmation flags[span_4](start_span)[span_4](end_span)[span_5](start_span)[span_5](end_span).
* *Operating System:* Windows host environment / Security lab utility suite[span_6](start_span)[span_6](end_span)[span_7](start_span)[span_7](end_span)[span_8](start_span)[span_8](end_span).
* *Tools Utilized:* 
  * *Johnny / John the Ripper:* Password cracking framework used for hash identification and dictionary/brute-force execution[span_9](start_span)[span_9](end_span)[span_10](start_span)[span_10](end_span)[span_11](start_span)[span_11](end_span).
  * *PDF Reader:* For validating successful decryption and viewing flag artifacts[span_12](start_span)[span_12](end_span).

---

## Methodology & Technical Workflow

### 1. Hash Identification and Extraction
When dealing with password-protected PDF files, modern security tools cannot attack the document directly through raw plaintext guesses at scale. Instead, the process involves:
* Inspecting the target PDF to evaluate its encryption standard (e.g., standard security handler, RC4, or AES encryption).
* Extracting the internal document hash format compatible with offline cracking tools. In this lab, the target hashes matched standard John the Ripper PDF parsing syntax (pdf$4*4*128*...)[span_13](start_span)[span_13](end_span)[span_14](start_span)[span_14](end_span)[span_15](start_span)[span_15](end_span).

### 2. Attack Execution (Dictionary / Brute-Force)
Using *Johnny*, the extracted hashes were loaded into the workspace interface[span_16](start_span)[span_16](end_span)[span_17](start_span)[span_17](end_span)[span_18](start_span)[span_18](end_span):
* Configured attack parameters to match target file signatures[span_19](start_span)[span_19](end_span)[span_20](start_span)[span_20](end_span)[span_21](start_span)[span_21](end_span).
* Applied targeted wordlists and rule sets designed to evaluate alphanumeric and symbolic variations.
* Monitored the cracking process until a 100% success rate was achieved across all target files[span_22](start_span)[span_22](end_span)[span_23](start_span)[span_23](end_span)[span_24](start_span)[span_24](end_span).

---

## Results & Findings

| Target File | Attack Method | Recovered Password | Status |
| :--- | :--- | :--- | :--- |
| *PDF Target 1* | Dictionary / Wordlist Match | good-luck[span_25](start_span)[span_25](end_span) | Cracked[span_26](start_span)[span_26](end_span) |
| *PDF Target 2* | Cryptanalytic/Pattern Assessment | password1[span_27](start_span)[span_27](end_span) | Cracked[span_28](start_span)[span_28](end_span) |
| *PDF Target 3* | Complex Character Mapping | 1qaz2wsx[span_29](start_span)[span_29](end_span) | Cracked[span_30](start_span)[span_30](end_span) |

Upon successful recovery, each password was used to decrypt its respective PDF file, revealing the confirmation flags (e.g., nw{cybersecurity_flag_captured_2608})[span_31](start_span)[span_31](end_span).

---

## Visual Evidence / Screenshots

* *Figure 1: Successful password recovery for Target 1 (good-luck)*
  ![PDF 1 Cracked Password](331996.jpg)[span_32](start_span)[span_32](end_span)

* *Figure 2: Successful password recovery for Target 2 (password1)*
  ![PDF 2 Cracked Password](332000.jpg)[span_33](start_span)[span_33](end_span)

* *Figure 3: Successful password recovery for Target 3 (1qaz2wsx)*
  ![PDF 3 Cracked Password](332006.jpg)[span_34](start_span)[span_34](end_span)

* *Figure 4: Final Flag Verification and Document Unlocking (nw{cybersecurity_flag_captured_2608})*
  ![Flag Captured](331114.jpg)[span_35](start_span)[span_35](end_span)

---

## Key Security Takeaways & Mitigation
* *Weak Passwords:* Passwords such as password1 or simple predictable strings are vulnerable to rapid dictionary and wordlist-based offline attacks.
* *Encryption Strength:* Even when strong underlying encryption standards (like AES) are used, overall file security is entirely dependent on the entropy and length of the user-chosen password.
* *Defense-in-Depth:* Organizations should enforce strict password complexity policies, implement multi-factor access controls, and avoid sharing sensitive documents protected by easily guessable credentials.

---

## Liability Disclaimer
> *Disclaimer:* The tools, techniques, and methodologies detailed in this repository are intended solely for educational purposes, authorized security testing, and completion of coursework for the Networkwalks Cybersecurity program. The author assumes no liability for the misuse of this information.
