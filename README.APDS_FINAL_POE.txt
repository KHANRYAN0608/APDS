International Payments Portal - Secure Employee & Customer Access

Project Overview
This project involves the development of a secure international payments portal for an international bank. It encompasses two primary access points:

Customer Portal: Allows customers to securely register, log in, and make international payments.
Employee Portal: Provides bank employees with access to verify and forward payments to the SWIFT system.
Both portals are built using React (frontend) and Node.js (backend), ensuring robust security and seamless user experience.

Objective

The goal is to ensure that sensitive customer information, such as personal details and payment transactions, is protected from common web vulnerabilities. This includes implementing strong password hashing, input validation, SSL encryption, and protection against attacks like SQL injection, XSS, CSRF, and DDoS.

Group Members

Gregory Mbiya - ST10090997
Zakariyyah Adams - ST10091209
Imaan Ebrahim - ST10021922
Jasmin Kisten - ST10025239
Ryan Khan - ST10155076
Kyle Govender - ST10090959

Features

Customer Portal
Registration: Customers can register using their full name, ID number, account number, and password. Passwords are securely hashed and salted using bcrypt before storage.
Login System: Users log in using their username, account number, and password to access the payment interface.
Payment Process: Customers enter the payment amount, select the currency, and input the recipient's SWIFT code and account details to initiate international transfers.
Data Security: All traffic is served over SSL for encrypted communication. Inputs are validated using RegEx patterns to prevent injection attacks.

Employee Portal
Pre-Registered Access: Employees are pre-registered, and no registration process is required. They simply log in with their employee credentials.
Transaction Verification: Employees can view incoming payment requests, verify the SWIFT code and recipient account details, and mark transactions as verified for forwarding to SWIFT.
Secure Submission: Once verified, employees submit the payments by clicking the "Submit to SWIFT" button.

Security Features

Password Security
Hashing & Salting: All passwords are securely hashed using bcrypt with a salt to protect user credentials from unauthorized access.
Input Whitelisting
RegEx Validation: All user inputs (e.g., payment amount, recipient details) are validated against strict RegEx patterns to ensure they conform to expected formats and prevent SQL injection and XSS.
SSL Encryption
All communications between the frontend (React) and backend (Node.js) are encrypted using SSL certificates to secure data in transit.
Protection Against Common Attacks
SQL Injection: Parameterized queries are used to prevent SQL injection vulnerabilities.
XSS (Cross-Site Scripting): All user input is sanitized to protect against malicious JavaScript code.
CSRF (Cross-Site Request Forgery): CSRF tokens are used to ensure that only authorized requests are accepted.
DDoS: Rate limiting and request throttling are implemented to protect against Distributed Denial of Service attacks.
DevSecOps Pipeline
A DevSecOps pipeline has been set up to ensure the security of the application throughout its lifecycle. This includes the following steps:

Code Quality: A SonarQube scan is run to identify code smells and security hotspots in the application code.
CI/CD: The pipeline is integrated with CircleCI to automatically trigger tests and security scans whenever new code is pushed to the repository.
Test Automation: Automated tests are run to validate the functionality and security of the application before deployment.
Getting Started
Follow these steps to get the project up and running locally:

Prerequisites
Make sure you have the following installed:

Node.js and npm (Node Package Manager)
React (for frontend)
MongoDB (for database)
Git (to clone the repository)
Cloning the Repository
Clone the repository:
bash
Copy code
git clone https://github.com/your-repository-url.git
Navigate into the project directory:
bash
Copy code
cd project-directory
Installing Dependencies
Run the following command to install all necessary dependencies:

bash
Copy code
npm install
Running the Project
Start the backend server:
bash
Copy code
npm run start-backend
Start the frontend React app:
bash
Copy code
npm start
Visit http://localhost:3000 in your browser to view the customer portal.

Running Tests
To run automated tests for the project, execute the following:

bash
Copy code
npm test
This will run the test suite and display any issues or failures.

Deployment
Once you're ready to deploy, build the project with:

bash
Copy code
npm run build
The build is optimized and ready to be deployed on a server.

Static Login for Employee Portal

In Task 3, the employee portal requires pre-configured user accounts. These accounts are hard-coded and do not require registration. They are automatically available once the system is deployed.

Security Considerations

The application is designed to protect sensitive customer and employee information. Key security practices have been implemented, including:

Two-factor authentication for employees (to be added in future updates).
Encryption of sensitive data (both at rest and in transit).
Auditing and logging of employee actions within the system.
Tools & Technologies Used
React - Frontend framework for building user interfaces.
Node.js - Backend framework for handling API requests.
bcrypt - Password hashing and salting.
RegEx - Input validation.
SSL - Encryption for secure data transmission.
CircleCI - Continuous Integration for testing and deployment.
SonarQube - Code quality and security scanning.
MongoDB - Database for storing user and transaction data.

Contributing

If you would like to contribute to the project, please follow these steps:
Fork the repository.
Create a feature branch (git checkout -b feature-name).
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature-name).
Open a pull request to merge your changes into the main branch.

License
This project is licensed under the MIT License - see the LICENSE.md file for details.