# BioAuthFortress - A Secure Biometric Authentication System

## Overview
BioAuthFortress is a Java-based biometric authentication system that securely enrolls and authenticates users using multiple biometric factors, such as fingerprints, facial recognition, and iris scans. The system employs AES encryption to protect biometric data and ensures secure session management for continuous authentication.

---

## 🔐 Features
- **Biometric Enrollment**: Users can register multiple biometric data types (fingerprints, facial, and iris scans).
- **Secure Storage**: Biometric templates are encrypted using AES with a unique key per user.
- **Liveness Detection**: Prevents spoofing by verifying biometric sample authenticity.
- **Session Management**: Maintains secure user sessions with token-based authentication.
- **Session Expiry**: Ensures security by automatically expiring inactive sessions.

---

## ⚙️ Technologies Used
- **Java**: Core programming language.
- **AES Encryption**: Securely encrypts biometric data.
- **UUID**: Generates session tokens.
- **SecureRandom**: Cryptographically secure random values for security mechanisms.

---

## 📋 Getting Started
### Prerequisites
- JDK 8 or later
- Recommended IDE: IntelliJ IDEA, Eclipse, or VS Code

### Installation
#### Clone the Repository
```bash
git clone <repository-url>
```

#### Set Up the Project
Navigate to the source directory:
```bash
cd BioAuthProject/src
```

#### Compile the Java Code
```bash
javac com/security/bioauth/BioAuthFortress.java
```

#### Run the Application
Since `BioAuthFortress` lacks a main method, integrate it into an existing system or create an entry point for testing.

---

## 🛠️ Usage
### Enrolling a User
```java
BioAuthFortress fortress = new BioAuthFortress();
fortress.enrollUser("user123", fingerprintData, facialData, irisData);
```

### Authenticating a User
```java
AuthenticationResult result = fortress.authenticate("user123", biometricSample);
System.out.println(result.getMessage());
```

### Verifying a Session
```java
boolean isValid = fortress.verifySession("user123", sessionToken);
System.out.println("Session valid: " + isValid);
```

---

## 🔐 Security Considerations
- **Encrypted Biometric Data**: AES encryption secures biometric templates.
- **Access Controls**: Restrict access to biometric data storage.
- **Session Expiry**: Sessions expire after inactivity (default: 15 minutes).

---

## 📜 License
This project is licensed under the **MIT License** - see the LICENSE file for details.

---

## 🤝 Contributing
We welcome contributions! Follow these steps:
1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/feature-name`.
3. Commit your changes: `git commit -am 'Add new feature'`.
4. Push the branch: `git push origin feature/feature-name`.
5. Create a new Pull Request.

---

## 📧 Contact
For questions or feedback, contact us at: 
📧 **Email:** bashconstanza@proton.me

🚀 **Made with ❤️ by constanza1110101**

