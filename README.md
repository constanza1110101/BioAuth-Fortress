# BioAuthFortress - A Secure Biometric Authentication System

## Overview

BioAuthFortress is a Java-based biometric authentication system that securely enrolls and authenticates users based on multiple biometric factors, such as fingerprints, facial recognition, and iris scans. The system uses AES encryption to store biometric data securely, ensuring that sensitive information is protected. It also provides session management for continuous authentication.

## Features

- **Biometric Enrollment**: Users can enroll with multiple biometric data types, including fingerprints, facial data, and iris scans.
- **Secure Storage**: Biometric templates are encrypted using AES (Advanced Encryption Standard) with a unique encryption key for each user.
- **Liveness Detection**: Ensures the authenticity of biometric samples with a liveness check.
- **Session Management**: Each successful authentication generates a session token, and users can remain authenticated within a session timeframe.
- **Session Expiry**: Sessions automatically expire after a specified duration, ensuring security after periods of inactivity.

## Technologies Used

- **Java**: The core programming language for the system.
- **AES Encryption**: Used for encrypting biometric data to ensure confidentiality.
- **UUID**: Generates session tokens for secure session management.
- **SecureRandom**: Used for generating cryptographically secure random values (e.g., session tokens and initialization vectors).

## Getting Started

### Prerequisites

- JDK 8 or later is required to compile and run the code.
- An IDE (such as IntelliJ IDEA, Eclipse, or Visual Studio Code) is recommended for development.

### Installation

1. **Clone the Repository:**

   ```bash
   git clone <repository-url>
Set Up the Project:

Navigate to the src directory where the BioAuthFortress.java file is located.

bash
Copiar código
cd BioAuthProject/src
Compile the Java Code:

If you are using the command line, use the javac command to compile the BioAuthFortress.java file:

bash
Copiar código
javac com/security/bioauth/BioAuthFortress.java
Run the Application:

Since the BioAuthFortress class doesn't contain a main method, you can integrate it into a larger application or write a main method for testing purposes. Alternatively, you can modify the code to create an entry point for demonstration.

Usage
Enroll a User: To enroll a user, provide their biometric data (fingerprint, facial, and iris samples) to the enrollUser method.

Authenticate a User: To authenticate a user, provide the user’s ID and a biometric sample. The system will verify the biometric data and return a session token if the authentication is successful.

Verify a Session: To verify an active session, provide the user ID and session token.

java
Copiar código
BioAuthFortress fortress = new BioAuthFortress();
fortress.enrollUser("user123", fingerprintData, facialData, irisData);
AuthenticationResult result = fortress.authenticate("user123", biometricSample);
System.out.println(result.getMessage());
Security Considerations
Biometric Data Storage: All biometric data (fingerprints, facial data, iris data) is encrypted using AES encryption before being stored. Only authorized personnel or systems can access the encrypted data.

Session Expiry: To ensure continuous security, sessions automatically expire after the session timeout period (set to 15 minutes by default).

License
This project is licensed under the MIT License - see the LICENSE file for details.

Contributing
We welcome contributions to improve BioAuthFortress. Please follow these guidelines:

Fork the repository.

Create a feature branch (git checkout -b feature/feature-name).

Commit your changes (git commit -am 'Add new feature').

Push to the branch (git push origin feature/feature-name).

Create a new Pull Request.

Contact
For questions or feedback, please contact us at bashconstanza@proton.me.

Made with ❤️ by constanza1110101

markdown
Copiar código

### Key Sections in the README:

- **Overview**: A brief description of what the project does.
- **Features**: A list of key features of the project.
- **Technologies Used**: The technologies and methods used in the project.
- **Getting Started**: Instructions on how to set up the project, including installation and compilation steps.
- **Usage**: How to use the methods in the `BioAuthFortress` class.
- **Security Considerations**: Key points on how biometric data is protected.
- **License**: Information on the project's license.
- **Contributing**: Guidelines for how others can contribute to the project.
- **Contact**: Contact information for questions or feedback.
