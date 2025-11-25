Below are **full, simple, exam-ready 10-mark answers** for **Q19, Q20, Q24**, written in clear language without jargon and easy to remember.

---

# **Q19. Differentiate between common web attacks and analyze the role of layered defense in preventing them**

Web systems face many attacks because they are publicly accessible.
Understanding the common attacks and how layered defense prevents them is essential for securing any website or online service.

---

# **1. Common Web Attacks**

## **1. Phishing**

* Trick users into revealing passwords or bank details.
* Usually sent as fake emails or fake login pages.
  **Goal:** Steal identity or financial information.

---

## **2. Cross-Site Scripting (XSS)**

* Attacker injects harmful scripts into websites.
* Script runs in the victim’s browser without their knowledge.
  **Goal:** Steal cookies, session IDs, or redirect users.

---

## **3. SQL Injection**

* Attacker sends harmful database queries through input fields.
  **Goal:** Access, delete, or modify database records.

---

## **4. Session Hijacking**

* Attacker steals the victim’s session ID (cookie).
  **Goal:** Log in as the victim without knowing the password.

---

## **5. Denial-of-Service (DoS)**

* Floods the server with traffic.
  **Goal:** Make the website slow or unavailable.

---

# **2. Why Do These Attacks Happen?**

* Poor input validation
* Weak authentication
* Exposed session information
* Unsecured network channels
* Lack of awareness among users

---

# **3. Role of Layered Defense in Preventing Attacks**

Layered defense is called **defense-in-depth**, meaning we protect the system at **multiple layers** so that if one layer fails, another layer stops the attack.

---

## **Layer 1: Input Validation**

* Blocks SQL injection and XSS
* Only allows safe input from users
* Rejects harmful scripts or queries

---

## **Layer 2: Authentication & Access Control**

* Multi-factor authentication prevents phishing-based account takeover
* Strong password rules
* Role-based access ensures attackers cannot access admin-level functions

---

## **Layer 3: Session Security**

* Secure & HttpOnly cookies
* Automatic session timeout
* Random session ID generation
  Prevents session hijacking.

---

## **Layer 4: Network Security**

* Firewalls block unknown or harmful traffic
* HTTPS encrypts data to prevent sniffing
* Proper server configuration prevents MITM attacks

---

## **Layer 5: User Awareness**

* Users trained to avoid phishing links
* Avoiding insecure downloads
* Checking website URLs before logging in

---

# **4. Advantages of Layered Defense**

* Covers weaknesses in any one layer
* Makes it difficult for attackers to succeed
* Ensures both technical and human protection
* Improves overall system strength

---

# **Conclusion**

Web attacks target weak points at many levels.
Layered defense protects every stage—user input, sessions, network, authentication—making the system resilient and secure even if one layer fails.

---

---

# **Q20. Examine the operational process of PGP and distinguish how its hybrid cryptographic approach enhances email security**

Pretty Good Privacy (PGP) is one of the most trusted methods for securing email communication. It protects **confidentiality, integrity, and authentication** using a combination of encryption and digital signatures.

---

# **1. Why PGP is Needed**

Emails travel across multiple servers.
Anyone intercepting the mail can read or modify it.
PGP solves this by:

* Encrypting the message
* Digitally signing it
* Ensuring only the intended receiver can open it

---

# **2. PGP Operational Process**

PGP works in three stages.

---

## **Stage 1: Key Generation**

Each user creates:

* A **public key** (shared with others)
* A **private key** (kept secret)

These keys are used for encryption and signing.

---

## **Stage 2: Email Encryption (Sender Side)**

### **Step 1: Create a session key**

A random symmetric key is generated.
This key will encrypt the message because it is **fast**.

### **Step 2: Encrypt the message**

Session key encrypts the email message.

### **Step 3: Encrypt the session key**

Session key is encrypted using receiver’s public key.

### **Step 4: Attach digital signature**

Sender signs the message using their private key.

---

## **Stage 3: Decryption (Receiver Side)**

### **Step 1: Decrypt session key**

Receiver uses their private key to unlock the session key.

### **Step 2: Decrypt message**

Session key decrypts the actual message.

### **Step 3: Verify signature**

Receiver uses sender’s public key to check authenticity.

---

# **3. How PGP’s Hybrid System Enhances Security**

PGP uses a combination of **symmetric** and **asymmetric** cryptography.

### **a) Symmetric Encryption**

* Fast
* Good for encrypting large emails
* Used for actual message encryption

### **b) Asymmetric Encryption**

* Very secure
* Used only to protect the session key
* Avoids the need for secret key sharing

---

# **4. Advantages of PGP’s Hybrid Approach**

### **Confidentiality**

Only the receiver can decrypt the session key and thus the message.

### **Integrity**

Message cannot be modified without changing the signature.

### **Authentication**

Digital signature confirms the identity of the sender.

### **Efficiency**

Combines the strength of public-key cryptography with the speed of symmetric encryption.

---

# **Conclusion**

PGP improves email security by combining the strengths of both encryption types.
Its hybrid model ensures that emails are safe, authentic, and protected from tampering.

---

---

# **Q24. Analyze the essential elements of web security and compare the effectiveness of layered defenses against phishing, XSS, and session hijacking**

Web security ensures safe communication, safe browsing, and protection of user data.
Different threats can target different parts of a website, so security must protect every part.

---

# **1. Essential Elements of Web Security**

### **1. Authentication**

Verifying who the user is.
Examples: passwords, OTP, biometrics.

### **2. Authorization**

Deciding what the user is allowed to do.
Prevents unauthorized access to admin areas.

### **3. Session Management**

Maintains user login state safely.
Uses cookies, timeouts, and secure tokens.

### **4. Data Protection**

Encrypting data in transit (HTTPS) and at rest.

### **5. Input Validation**

Ensures user inputs do not contain harmful code.
First defense against injection attacks and XSS.

### **6. Error Handling**

Prevents revealing sensitive internal details.

### **7. Logging and Monitoring**

Detects suspicious activities, failed logins, and potential attacks.

---

# **2. Common Attacks and How Layered Defense Combats Them**

## **a) Phishing**

Attackers trick users into entering credentials on fake websites.

### **Layered Defense**

* Multi-factor authentication
* Browser warnings
* Email filtering
* User awareness training

**Effectiveness:**
Strong, because even if users fall for phishing, OTP/MFA blocks attackers.

---

## **b) Cross-Site Scripting (XSS)**

Malicious script injected into web pages.

### **Layered Defense**

* Input sanitization
* Output encoding
* Using Content-Security-Policy (CSP)
* Blocking unsafe scripts

**Effectiveness:**
Very high, because filtering at multiple layers prevents script execution.

---

## **c) Session Hijacking**

Attacker steals session cookies.

### **Layered Defense**

* Secure & HttpOnly cookies
* Session timeout
* Regenerate session IDs after login
* End-to-end HTTPS

**Effectiveness:**
High when using secure cookies + HTTPS, because attackers cannot steal session tokens easily.

---

# **3. Why Layered Defense Works Better Than Single Solutions**

* Attacks occur at different layers
* One failure does not cause complete system compromise
* Protects users, servers, sessions, and data
* Reduces damage even if an attack succeeds partially

---

# **Conclusion**

Strong web security depends on multiple layers—authentication, input filtering, secure sessions, encryption, and user awareness. A layered approach effectively protects against major threats like phishing, XSS, and session hijacking by blocking attacks at different points in the system.

---

If you want, I can prepare the **remaining questions Q19–Q25** or create a **full revision sheet for all units**.
