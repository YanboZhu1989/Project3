# Skillified: Your On-chain Education Platform
![login_page](resources/readme_images/login_page.png)
## Overview
Skillified is an on-chain education platform that facilitates the creation, enrollment, and certification of courses. By leveraging the Ethereum blockchain and IPFS, the platform ensures the integrity, transparency, and verifiability of educational achievements. The system is divided into three main user roles: **Admin**, **Instructor**, and **Student**. Each role has specific functions and capabilities to interact with the platform.

## Features
### Web3 Login Page
**How It Works**

1. **Select Ethereum Address**: Users are presented with a dropdown containing available Ethereum addresses. This selection simulates the process of connecting a Web3 wallet.

2. **Login Button**: Upon selecting an address, users can click the "Login" button to access the platform.

3. **Role Selection**: After logging in, users are directed to a navigation sidebar where they can select their role as Admin, Instructor, or Student. Each role provides unique functionalities and access within the platform.

4. **Logout Functionality**: A logout button in the navigation sidebar allows users to log out, returning them to the main page. This makes it possible to select a different account or simply exit the application.

5. **Session Management**: The login and logout functionalities are supported by Streamlit's session state management, ensuring that user selections and actions are preserved across different parts of the application.

### Benefits
- **Enhanced User Experience**: The login page provides an intuitive and familiar experience, aligning with typical decentralised applications.

- **Role-Based Access**: By allowing users to select roles, the platform can tailor the experience and features available to each user type.

- **Flexibility**: The login page serves as a gateway to the platform, allowing easy navigation and control over user interactions.
---
### Admin Portal
![admin_portal_1](resources/readme_images/admin_portal_1.png)
![admin_portal_2](resources/readme_images/admin_portal_2.png)

- **Create Courses**: Define course titles, instructors, associated material (via IPFS), exams, and fees.

- **Upload Materials**: Upload course content and certificate images to IPFS.
---
### Instructor Portal
![instructor_portal_1](resources/readme_images/instructor_portal_1.png)
![instructor_portal_2](resources/readme_images/instructor_portal_2.png)
- **View Enrollments**: Access student enrollment details, including names, addresses, enrollment dates, exam statuses, and completion dates.

- **Mark Completion**: Mark a course as completed and issue a certificate to a student.
---
### Student Portal
![student_portal](resources/readme_images/student_portal.png)
- **Enroll in Courses**: Browse available courses, enroll by paying the required fee, and provide a name for certification.

- **Access Course Material**: Access course material hosted on IPFS.

- **Take Exams**: Participate in exams to demonstrate competence.

- **View Certificates**: View and access certificates of completed courses.

## Certificates
Once the user has enrolled and viewed the course material they are prompted to take the exam, which is 10 multiple choice questions that directly correspond to the course material. Once the student has submitted their exam the result is recorded on chain and if the student passed the exam a certificate of completion for the course is issued & displays in the student portal under the "My Certificates" title.

![my_certificates](resources/readme_images/my_certificates.png)

## Smart Contract Structure
The platform is underpinned by a Solidity smart contract that utilises ERC721Enumerable for certificate issuance.

**Key structures include**:

- **Course**: Contains information about the course such as title, instructor, IPFS hash for material, exam title, certificate IPFS hash, status, and fee.

- **Enrollment**: Records details about student enrollments, including course ID, student address, name, completion status, and date.

- **Certificate**: Details the certificate issued to a student, including student name, course title, certificate IPFS hash, and completion date.

- **QuizResult**: Records the exam results for students, including course ID, student address, pass status, and timestamp.

## Dependencies
- **Solidity ^0.8.1**: For smart contract development.

- **OpenZeppelin**: Utilised for the ERC721Enumerable extension.

- **Web3**: For interacting with the Ethereum blockchain.

- **Streamlit**: For building the front-end interface.

- **IPFS**: For decentralised storage of course materials and certificates.

- **Pinata**: For pinning files to IPFS.

## Setup
1. **Compile the Contract**: Compile the Solidity contract in the appropriate environment.

2. **Configure Environment Variables**: Set up .env file with WEB3_RPC, SMART_CONTRACT_ADDRESS, PINATA_API_KEY, and PINATA_SECRET_API_KEY.

3. **Connect to Ethereum Network**: Ensure that the provided RPC URL in the environment variables is accessible.

4. **Run the Application**: Start the Streamlit application.

## Conclusion
Skillified is a novel approach to education that leverages blockchain technology to bring transparency and authenticity to the learning process. By certifying skills on-chain, it opens new opportunities for learners and educators, promoting trust and collaboration in the educational ecosystem.





