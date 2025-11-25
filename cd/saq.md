# Network Security - 100 Short Answer Questions (1 Mark)

## UNIT I - Security Concepts & Cryptography Basics (20 Questions)

**Q1. What is information security?**
A: Information security is the practice of protecting information from unauthorized access, use, disclosure, disruption, modification, or destruction.

**Q2. What are the three main security goals (CIA triad)?**
A: Confidentiality, Integrity, and Availability.

**Q3. Define Confidentiality.**
A: Confidentiality ensures that information is accessible only to authorized individuals or systems.

**Q4. Define Integrity.**
A: Integrity ensures that information remains accurate, complete, and unaltered by unauthorized parties.

**Q5. Define Availability.**
A: Availability ensures that information and resources are accessible to authorized users when needed.

**Q6. What is a passive attack?**
A: A passive attack monitors or eavesdrops on communications without modifying data, such as traffic analysis or message interception.

**Q7. What is an active attack?**
A: An active attack involves modification of data or creation of false data streams, such as masquerading, replay, or denial of service.

**Q8. What is cryptography?**
A: Cryptography is the science of securing communication by transforming information into an unreadable format using mathematical techniques.

**Q9. What is plaintext?**
A: Plaintext is the original readable message or data before encryption.

**Q10. What is ciphertext?**
A: Ciphertext is the encrypted, unreadable form of plaintext after applying an encryption algorithm.

**Q11. What is encryption?**
A: Encryption is the process of converting plaintext into ciphertext using an algorithm and a key.

**Q12. What is decryption?**
A: Decryption is the process of converting ciphertext back into plaintext using an algorithm and a key.

**Q13. What is a substitution cipher?**
A: A substitution cipher replaces each character in plaintext with another character according to a fixed system.

**Q14. What is a transposition cipher?**
A: A transposition cipher rearranges the positions of characters in plaintext without changing the characters themselves.

**Q15. What is symmetric key cryptography?**
A: Symmetric key cryptography uses the same key for both encryption and decryption.

**Q16. What is asymmetric key cryptography?**
A: Asymmetric key cryptography uses a pair of keys - a public key for encryption and a private key for decryption.

**Q17. What is a security service?**
A: A security service is a processing or communication service that enhances the security of data processing systems and information transfers.

**Q18. What is authentication?**
A: Authentication is the process of verifying the identity of a user, device, or system.

**Q19. What is non-repudiation?**
A: Non-repudiation prevents a sender from denying that they sent a message or performed an action.

**Q20. What is access control?**
A: Access control restricts access to resources based on the identity and authorization level of users.

---

## UNIT II - Symmetric & Asymmetric Ciphers (20 Questions)

**Q21. What is a block cipher?**
A: A block cipher encrypts data in fixed-size blocks (typically 64 or 128 bits) using a symmetric key.

**Q22. What does DES stand for?**
A: DES stands for Data Encryption Standard.

**Q23. What is the key size of DES?**
A: DES uses a 56-bit key (64 bits including parity bits).

**Q24. What is the block size of DES?**
A: DES operates on 64-bit blocks of data.

**Q25. What does AES stand for?**
A: AES stands for Advanced Encryption Standard.

**Q26. What are the key sizes supported by AES?**
A: AES supports key sizes of 128, 192, and 256 bits.

**Q27. What is the block size of AES?**
A: AES operates on 128-bit blocks of data.

**Q28. What is a stream cipher?**
A: A stream cipher encrypts data one bit or byte at a time using a keystream.

**Q29. What is the main advantage of stream ciphers?**
A: Stream ciphers are faster and more suitable for real-time applications with continuous data streams.

**Q30. Name one popular stream cipher.**
A: RC4 is a popular stream cipher (though now considered insecure).

**Q31. What is the Feistel structure?**
A: The Feistel structure is a symmetric cipher design where encryption operates on half the data block in each round, used in DES.

**Q32. How many rounds does DES have?**
A: DES has 16 rounds of processing.

**Q33. How many rounds does AES have for 128-bit keys?**
A: AES has 10 rounds for 128-bit keys.

**Q34. What is public key cryptography?**
A: Public key cryptography uses a pair of mathematically related keys where one key encrypts and the other decrypts.

**Q35. Who developed the RSA algorithm?**
A: RSA was developed by Rivest, Shamir, and Adleman in 1977.

**Q36. What mathematical problem is RSA based on?**
A: RSA is based on the difficulty of factoring large prime numbers.

**Q37. What is the Diffie-Hellman algorithm used for?**
A: Diffie-Hellman is used for secure key exchange over an insecure channel.

**Q38. What is the main advantage of asymmetric cryptography?**
A: It eliminates the need for secure key exchange as the public key can be freely distributed.

**Q39. What is the main disadvantage of asymmetric cryptography?**
A: It is significantly slower than symmetric cryptography.

**Q40. What is IDEA?**
A: IDEA (International Data Encryption Algorithm) is a symmetric block cipher that operates on 64-bit blocks with a 128-bit key.

---

## UNIT III - Hash Functions & Key Management (20 Questions)

**Q41. What is a cryptographic hash function?**
A: A hash function takes input data of any size and produces a fixed-size output called a hash or digest.

**Q42. What are the main properties of a good hash function?**
A: One-way (irreversible), collision-resistant, and deterministic output for the same input.

**Q43. What does MD5 stand for?**
A: MD5 stands for Message Digest Algorithm 5.

**Q44. What is the output size of MD5?**
A: MD5 produces a 128-bit (16-byte) hash value.

**Q45. Is MD5 still considered secure?**
A: No, MD5 is considered cryptographically broken and unsuitable for security applications.

**Q46. What does SHA stand for?**
A: SHA stands for Secure Hash Algorithm.

**Q47. What is the output size of SHA-512?**
A: SHA-512 produces a 512-bit (64-byte) hash value.

**Q48. What is message authentication?**
A: Message authentication verifies that a message has not been altered and confirms the sender's identity.

**Q49. What does MAC stand for?**
A: MAC stands for Message Authentication Code.

**Q50. What is HMAC?**
A: HMAC (Hash-based Message Authentication Code) is a MAC that uses a cryptographic hash function with a secret key.

**Q51. What is a digital signature?**
A: A digital signature is a cryptographic mechanism that provides authentication, integrity, and non-repudiation using asymmetric cryptography.

**Q52. How does a digital signature work?**
A: The sender encrypts a message hash with their private key; the receiver decrypts it with the sender's public key to verify.

**Q53. What is key distribution?**
A: Key distribution is the process of securely delivering cryptographic keys to authorized parties.

**Q54. What is a Key Distribution Center (KDC)?**
A: A KDC is a trusted third party that manages and distributes secret keys to users in a network.

**Q55. What is Kerberos?**
A: Kerberos is a network authentication protocol that uses symmetric key cryptography and a trusted third party (KDC).

**Q56. What is X.509?**
A: X.509 is a standard that defines the format of public key certificates for authentication.

**Q57. What is a digital certificate?**
A: A digital certificate is an electronic document that binds a public key to an entity's identity, signed by a trusted authority.

**Q58. What is PKI?**
A: PKI (Public Key Infrastructure) is a framework for managing digital certificates and public-private key pairs.

**Q59. What is a Certificate Authority (CA)?**
A: A CA is a trusted entity that issues, manages, and revokes digital certificates.

**Q60. What is certificate revocation?**
A: Certificate revocation is the process of invalidating a certificate before its expiration date due to compromise or other reasons.

---

## UNIT IV - IP Security (20 Questions)

**Q61. What is IPSec?**
A: IPSec (Internet Protocol Security) is a protocol suite for securing IP communications through authentication and encryption.

**Q62. At which OSI layer does IPSec operate?**
A: IPSec operates at the Network Layer (Layer 3).

**Q63. What are the two main protocols in IPSec?**
A: Authentication Header (AH) and Encapsulating Security Payload (ESP).

**Q64. What does AH provide?**
A: AH provides data integrity, authentication, and anti-replay protection but not confidentiality.

**Q65. What does ESP provide?**
A: ESP provides confidentiality, data integrity, authentication, and anti-replay protection.

**Q66. What are the two modes of IPSec operation?**
A: Transport mode and Tunnel mode.

**Q67. What is Transport mode in IPSec?**
A: Transport mode encrypts only the payload of the IP packet, leaving the original IP header intact.

**Q68. What is Tunnel mode in IPSec?**
A: Tunnel mode encrypts the entire IP packet and adds a new IP header, commonly used for VPNs.

**Q69. What is a Security Association (SA)?**
A: An SA is a one-way logical connection that defines security parameters between two communicating parties in IPSec.

**Q70. What is the Security Parameter Index (SPI)?**
A: SPI is a unique identifier used to identify a specific Security Association in IPSec.

**Q71. What is IKE?**
A: IKE (Internet Key Exchange) is a protocol used to establish and manage Security Associations in IPSec.

**Q72. What are the two phases of IKE?**
A: Phase 1 establishes a secure channel (ISAKMP SA), and Phase 2 negotiates IPSec SAs for data protection.

**Q73. What port does IKE use?**
A: IKE uses UDP port 500.

**Q74. What is anti-replay protection?**
A: Anti-replay protection prevents attackers from capturing and retransmitting packets by using sequence numbers.

**Q75. Can AH and ESP be used together?**
A: Yes, AH and ESP can be combined to provide both authentication and encryption.

**Q76. What is the IPSec Security Policy Database (SPD)?**
A: SPD defines the security policies that determine how IP packets are processed (protected, bypassed, or discarded).

**Q77. What is the Security Association Database (SAD)?**
A: SAD stores information about active Security Associations including keys, algorithms, and parameters.

**Q78. What is Perfect Forward Secrecy (PFS)?**
A: PFS ensures that compromising one session key does not compromise past or future session keys.

**Q79. What is NAT-T in IPSec?**
A: NAT-T (NAT Traversal) allows IPSec traffic to pass through Network Address Translation devices.

**Q80. Why is NAT-T needed for IPSec?**
A: NAT modifies IP headers which breaks IPSec's integrity checks; NAT-T encapsulates IPSec in UDP to solve this.

---

## UNIT V - Web Security (20 Questions)

**Q81. What are the main web security threats?**
A: Main threats include eavesdropping, data modification, identity spoofing, and denial of service attacks.

**Q82. What does PGP stand for?**
A: PGP stands for Pretty Good Privacy.

**Q83. What is PGP used for?**
A: PGP is used for encrypting and decrypting emails, files, and directories, and for digital signatures.

**Q84. What type of encryption does PGP use?**
A: PGP uses hybrid encryption combining symmetric and asymmetric cryptography.

**Q85. What does S/MIME stand for?**
A: S/MIME stands for Secure/Multipurpose Internet Mail Extensions.

**Q86. What is S/MIME used for?**
A: S/MIME is used for sending digitally signed and encrypted email messages.

**Q87. What does SSL stand for?**
A: SSL stands for Secure Sockets Layer.

**Q88. What does TLS stand for?**
A: TLS stands for Transport Layer Security.

**Q89. What is the relationship between SSL and TLS?**
A: TLS is the successor to SSL, providing improved security; they are often used interchangeably.

**Q90. At which OSI layer does SSL/TLS operate?**
A: SSL/TLS operates between the Transport Layer and Application Layer (Session Layer).

**Q91. What port does HTTPS use?**
A: HTTPS uses TCP port 443.

**Q92. What is the SSL/TLS handshake?**
A: The handshake is a process where client and server negotiate encryption parameters, authenticate, and establish session keys.

**Q93. What does SET stand for?**
A: SET stands for Secure Electronic Transaction.

**Q94. What is SET used for?**
A: SET is a protocol for securing credit card transactions over the internet.

**Q95. What are the main components of SSL/TLS?**
A: The Handshake Protocol, Record Protocol, Alert Protocol, and Change Cipher Spec Protocol.

**Q96. What is a digital certificate's role in SSL/TLS?**
A: Digital certificates authenticate the server's identity to the client during the SSL/TLS handshake.

**Q97. What is session resumption in SSL/TLS?**
A: Session resumption allows clients to reconnect to a server using previously negotiated security parameters without a full handshake.

**Q98. What is the purpose of the SSL/TLS Record Protocol?**
A: The Record Protocol fragments, compresses, encrypts, and authenticates data for transmission.

**Q99. What is a man-in-the-middle attack?**
A: An attack where an attacker intercepts and possibly alters communications between two parties without their knowledge.

**Q100. How does SSL/TLS prevent man-in-the-middle attacks?**
A: Through server authentication using digital certificates signed by trusted Certificate Authorities and encrypted key exchange.