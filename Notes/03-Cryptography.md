# 🔑 Cryptography Basics

## 1. Symmetric vs. Asymmetric Encryption

### Symmetric Encryption
Uses a **single shared key** for both encryption and decryption.
*   *Pros:* Extremely fast and computationally efficient.
*   *Cons:* Difficult key distribution problem (how to securely share the secret key).
*   *Algorithms:* AES (Advanced Encryption Standard), DES, 3DES.

### Asymmetric Encryption
Uses a mathematically tied **key pair**: a **Public Key** (shared with everyone for encryption) and a **Private Key** (kept secret by the owner for decryption).
*   *Pros:* Solves the key exchange issue.
*   *Cons:* Slower and resource-heavy.
*   *Algorithms:* RSA, ECC (Elliptic Curve Cryptography).

---

## 2. Cryptographic Hashing
A cryptographic hash function maps input data of arbitrary length into a deterministic, fixed-size string of characters.
*   **Properties:** One-way (cannot be reversed), collision-resistant (two inputs cannot produce the same hash), and deterministic.
*   **Common Hashing Algorithms:**
    *   **MD5:** 128-bit hash. Cryptographically broken (vulnerable to collision attacks).
    *   **SHA-256:** 256-bit hash. Part of the SHA-2 family. Currently secure and widely used for integrity checks.

---

## 3. Digital Certificates & SSL/TLS
*   **Digital Certificates:** Electronic credentials issued by a trusted Third-Party Certificate Authority (CA). They verify the true identity of a website or server.
*   **SSL/TLS Handshake:** The process that establishes an encrypted communication tunnel over HTTPS:
    1.  Client hello, server hello with its certificate.
    2.  Verification of server certificate by the browser.
    3.  Key exchange to establish a shared symmetric session key for fast, secure web browsing.

---

## 4. Hands-on OpenSSL Exercises
Commands to encrypt, decrypt, and hash messages inside a Kali Linux terminal:

### Encrypting a Message (Symmetric AES-256)
```bash
echo "TopSecretMessage" > plain.txt
openssl enc -aes-256-cbc -salt -in plain.txt -out encrypted.enc
