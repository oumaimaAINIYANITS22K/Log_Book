# Project Logbook  

This logbook records the daily activities and progress of the project. Each entry lists the hours spent, the focus of the work, and the output generated.  

| Date      | Used Hours | Subject(s)   | Output          |
|-----------|------------|--------------|-----------------|
| 17.1.2025 | 2          | Kick-off lecture | Accomplishing the test and looking into resources |
| 23.1.2025 | 3          | Second lecture | Understanding of the foundation that the course will be built on |
| 25.1.2025 | 1:30       | Logbook        | Doing the logbook assignment and looking into the materials     |
| 3.2.2025  | 2:30       | Studying course materials | Getting familiar with security concepts and Burp Suite environment |
| 4.2.2025  | 3          | Studying course materials | Understanding web security vulnerabilities and testing methodologies |
| 5.2.2025  | 3:30       | Practicing with PortSwigger | Exploring tools and workflows to interact with web applications |
| 6.2.2025  | 2:45       | Testing methodologies | Setting up intercepting proxy configurations and analyzing HTTP traffic |
| 7.2.2025  | 3:15       | Practicing vulnerability discovery | Learning how to identify and exploit common security flaws |
| 8.2.2025  | 4          | Preparing for lab completion | Reviewing study materials and refining methodologies |
| 9.2.2025  | 8          | Completed all labs | Finished all assigned labs and documented reflections |
| 19.2.2025 | 10         | **Penetration Testing on Booking System - Phase 1 (Day 1)** | Setting up VirtualBox & Kali Linux, installing required tools (Docker, ZAP, Burp), cloning & running the test application |
| 20.2.2025 | 12         | **Penetration Testing on Booking System - Phase 1 (Day 2)** | Conducted penetration tests, identified vulnerabilities (plaintext passwords, SQLi, privilege escalation), wrote and submitted the report |
| 5.3.2025  | 7          | **Penetration Testing on Booking System - Phase 2** | Conducted additional penetration tests using ZAP by Checkmarx, investigated API response inconsistencies, and updated security findings |
| 16.3.2025 | 6          | **MD5 Hash Cracking & Password Recovery** | Used Hashcat with RockYou, online hash lookup services, and brute-force attempts to crack password hashes. Found 7/10 passwords but brute-force estimates exceeded 30+ years for the rest. |

---

## **New Reflection: MD5 Hash Cracking & Password Recovery (16.3.2025)**
Spent **6 hours** working on **password cracking techniques** using **Hashcat and online lookup services**.  

### **Approach & Findings**
1. **Dictionary Attack**  
   - Used **Hashcat** with **RockYou.txt**.  
   - Cracked several common passwords but some remained unknown.  

2. **Online Hash Lookup Services**  
   - Tested sites like **Reverse Hash Lookup, Hashes.org, MD5Online, and LeakedPassword**.  
   - Retrieved a few additional passwords from these databases.  

3. **Brute-Force Testing**  
   - Attempted **custom brute-force attack** with varying lengths.  
   - **Final estimation: 30+ years** required to crack remaining hashes.  
   - **Conclusion:** Impractical to continue brute-force attempts.  

### **Outcome**
✅ **7 out of 10 passwords cracked.**  
✅ **Online hash lookup services were the fastest method.**  
❌ **Brute-force cracking was infeasible due to extreme time estimates.**  

This task provided valuable hands-on experience in **password security** and **real-world cracking limitations**. Future work will focus on **more advanced attack methods** and **optimization techniques**.


---

## **Reflections**

### **Username Enumeration via Different Responses**
This lab highlighted how inconsistent login error messages can be exploited to identify valid usernames. The challenge was recognizing subtle differences in response behavior and automating the process efficiently.

### **2FA Simple Bypass**
I learned that weak implementations of two-factor authentication, such as predictable codes or bypassing via session hijacking, can lead to security breaches. The most challenging part was identifying a practical bypass method and testing it effectively.

### **Password Reset Broken Logic**
This lab demonstrated how insecure password reset flows can be exploited. Understanding how to manipulate reset tokens or email verification steps was insightful. The hardest part was constructing a valid exploit chain.

### **Unprotected Admin Functionality**
This exercise showed how missing authentication layers on admin panels can expose sensitive functionalities. The key takeaway was the importance of proper access controls.

### **Unprotected Admin Functionality with Unpredictable URL**
Even if an admin panel isn't directly linked, attackers can discover it through various techniques. The main challenge was locating the hidden admin panel and bypassing access restrictions.

### **User Role Controlled by Request Parameter**
Here, I exploited the ability to change user roles through insecure request parameters. It emphasized the importance of server-side validation to prevent privilege escalation.

### **SQL Injection - Hidden Data Retrieval**
I learned how SQL injection can be used to extract hidden database content. Crafting the right queries without triggering security defenses was the tricky part.

### **SQL Injection - Login Bypass**
By injecting SQL payloads into login forms, I managed to authenticate without valid credentials. This lab reinforced the importance of prepared statements to prevent such attacks.

---

## **New Reflection: Penetration Testing on Booking System (19-20.2.2025 & 5.3.2025)**
I spent **two days (20 hours total) on Phase 1** and **an additional 7 hours on Phase 2**, conducting a **full penetration test** on the **Booking System’s registration page**.  

### **Phase 1: Initial Penetration Testing (19-20.2.2025)**
#### **Day 1 (19.2.2025): Setting Up the Environment**
- Installed **VirtualBox & Kali Linux**.
- Installed **Docker, OWASP ZAP, and Burp Suite** for penetration testing.
- Cloned the **Booking System repository** and deployed the app with **Docker Compose**.
- Confirmed that the system was **running on localhost**.

#### **Day 2 (20.2.2025): Penetration Testing & Reporting**
- **Tested the registration system** for vulnerabilities.
- **Key Findings:**
  - **Plaintext Password Storage** 🛑 (**Critical**)  
    - The database stored passwords in **plaintext** instead of using **bcrypt hashing**.
    - **Fix:** Implement bcrypt hashing before storing credentials.
  
  - **SQL Injection Vulnerability** ⚠ (**Medium**)  
    - The registration form allowed SQL injection via input fields.
    - **Fix:** Use **prepared statements** and input validation.
  
  - **Insecure User Role Assignment** ⚠ (**Medium**)  
    - Users could escalate privileges by modifying request parameters.
    - **Fix:** Enforce **server-side role validation**.

- **Created a penetration testing report** (`report.md`).
- **Pushed the findings to GitHub** and submitted the report.
- **Posted vulnerability findings** in the discussion forum.

### **Phase 2: Updated Penetration Testing (5.3.2025)**
- Conducted an **updated scan using ZAP by Checkmarx**.
- **Investigated API response inconsistencies** with different User-Agent headers.
- **Key Finding:**
  - **User-Agent Fuzzer Alert** ⚠ (**Medium**)
    - The system responded **differently** to requests with different **User-Agent headers**.
    - **Fix:** Ensure uniform response handling for all User-Agent headers.
- **Updated the penetration testing report with new findings**.

---

## **Conclusion**
Completing these labs and penetration tests was an insightful experience that reinforced my understanding of web security vulnerabilities. I spent time getting familiar with security tools, setting up test environments, and refining my testing methodologies. The hands-on approach helped me build confidence in identifying and mitigating security risks.  

Going forward, I plan to explore **more advanced vulnerabilities** and improve my **exploitation techniques**. This logbook will be updated regularly to track future progress and learning. 🚀
