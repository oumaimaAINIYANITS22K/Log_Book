# Project Logbook

This logbook records the daily activities and progress of the project. Each entry lists the hours spent, the focus of the work, and the output generated.

| Date      | Used Hours | Subject(s)   | Output          |
|-----------|------------|--------------|-----------------|
| 17.1.2025| 2          | Kick-off lecture | Accomplishing the test and looking into resources |
| 23.1.2025| 3          | Second lecture | Understanding of the foundation that the course will be built on |
| 25.1.2025| 1:30       | Logbook        | Doing the logbook assignment and looking into the materials     |
| 3.2.2025 | 2:30       | Studying course materials | Getting familiar with security concepts and Burp Suite environment |
| 4.2.2025 | 3          | Studying course materials | Understanding web security vulnerabilities and testing methodologies |
| 5.2.2025 | 3:30       | Practicing with PortSwigger | Exploring tools and workflows to interact with web applications |
| 6.2.2025 | 2:45       | Testing methodologies | Setting up intercepting proxy configurations and analyzing HTTP traffic |
| 7.2.2025 | 3:15       | Practicing vulnerability discovery | Learning how to identify and exploit common security flaws |
| 8.2.2025 | 4          | Preparing for lab completion | Reviewing study materials and refining methodologies |
| 9.2.2025 | 8          | Completed all labs | Finished all assigned labs and documented reflections |

## Reflections

### Username Enumeration via Different Responses
This lab highlighted how inconsistent login error messages can be exploited to identify valid usernames. The challenge was recognizing subtle differences in response behavior and automating the process efficiently.

### 2FA Simple Bypass
I learned that weak implementations of two-factor authentication, such as predictable codes or bypassing via session hijacking, can lead to security breaches. The most challenging part was identifying a practical bypass method and testing it effectively.

### Password Reset Broken Logic
This lab demonstrated how insecure password reset flows can be exploited. Understanding how to manipulate reset tokens or email verification steps was insightful. The hardest part was constructing a valid exploit chain.

### Unprotected Admin Functionality
This exercise showed how missing authentication layers on admin panels can expose sensitive functionalities. The key takeaway was the importance of proper access controls.

### Unprotected Admin Functionality with Unpredictable URL
Even if an admin panel isn't directly linked, attackers can discover it through various techniques. The main challenge was locating the hidden admin panel and bypassing access restrictions.

### User Role Controlled by Request Parameter
Here, I exploited the ability to change user roles through insecure request parameters. It emphasized the importance of server-side validation to prevent privilege escalation.

### SQL Injection - Hidden Data Retrieval
I learned how SQL injection can be used to extract hidden database content. Crafting the right queries without triggering security defenses was the tricky part.

### SQL Injection - Login Bypass
By injecting SQL payloads into login forms, I managed to authenticate without valid credentials. This lab reinforced the importance of prepared statements to prevent such attacks.

## Conclusion
Completing these labs was an insightful experience that reinforced my understanding of web security vulnerabilities. I spent time getting familiar with the PortSwigger environment, setting up tools, and refining my testing methodologies. The hands-on approach helped me build confidence in identifying and mitigating security risks. Going forward, I plan to explore more advanced vulnerabilities and improve my exploitation techniques. This logbook will be updated regularly to track future progress and learning.

