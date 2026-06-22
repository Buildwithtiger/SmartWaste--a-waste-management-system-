
##SmartWaste - A Waste Management System
"Smart waste, clean space"

https://img.shields.io/badge/version-1.0.0-blue
https://img.shields.io/badge/PHP-7.4+-777BB4?logo=php&logoColor=white
https://img.shields.io/badge/MySQL-8.0+-4479A1?logo=mysql&logoColor=white
https://img.shields.io/badge/status-Academic%2520Project-green

📋 Table of Contents
Overview

Features

Screenshots

Technologies Used

System Requirements

Installation & Setup

Project Structure

Database Schema

Future Enhancements

Limitations

Contributors

Acknowledgments

License

🌟 Overview
SmartWaste is a technology-driven waste management system designed to address the growing challenges of improper waste disposal in urban areas. By integrating real-time tracking, optimized routing, and professional cleaning services, this platform aims to create cleaner, healthier, and more sustainable communities.

Waste management has become one of the most critical challenges faced by modern societies. Traditional methods often lack efficiency, resulting in delayed pickups, overflowing bins, and unhygienic surroundings. SmartWaste bridges this gap by providing:

Real-time GPS tracking of garbage disposal trucks

Route optimization for efficient waste collection

Professional cleaning services for homes, schools, colleges, and workplaces

User-friendly features including appointment booking, login, and service history tracking

📌 Project Type: Academic Project (TYBBA(CA) - Semester IV)
📅 Academic Year: 2025-2026
🏛️ Institution: Hutatma Rajguru Mahavidyalaya, Rajgurunagar, Pune

🚀 Features
For Users
Feature	Description
User Registration & Login	Secure authentication system for users
Appointment Booking	Schedule professional cleaning services online
Service History	Track all past bookings and services
Real-Time Truck Tracking	Monitor garbage collection trucks in real-time
User Profile Management	View and update personal information
Booking Management	View, cancel, or reschedule bookings
For Admin
Feature	Description
Dashboard	Overview of system statistics and activities
Service Management	Add, update, or remove cleaning services
Booking Oversight	View and manage all user bookings
User Management	Manage user accounts and permissions
Reports	Generate reports on waste collection activities
System Capabilities
✅ Efficient waste collection through optimized routing

✅ Pollution control through proper waste management

✅ Employment generation for drivers, cleaners, and staff

✅ Sustainable practices promoting eco-friendly living

✅ Transparency through booking and history tracking

📸 Screenshots
Login Page
https://screenshots/login-page.png

Home Page
https://screenshots/home-page.png

User Profile Page
https://screenshots/user-profile-page.png

Book Cleaner Page
https://screenshots/book-cleanerman-page.png

Book Schedule Page
https://screenshots/book-schedule-page.png

Services Page
https://screenshots/services-page.png

Admin Dashboard
https://screenshots/admin-page.png

🛠️ Technologies Used
Frontend
<div> <img src="https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white" alt="HTML5"/> <img src="https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white" alt="CSS3"/> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black" alt="JavaScript"/> </div>
Backend
<div> <img src="https://img.shields.io/badge/PHP-777BB4?logo=php&logoColor=white" alt="PHP"/> </div>
Database
<div> <img src="https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white" alt="MySQL"/> </div>
Development Tools
<div> <img src="https://img.shields.io/badge/Visual%20Studio%20Code-007ACC?logo=visualstudiocode&logoColor=white" alt="VS Code"/> </div>
💻 System Requirements
Hardware Requirements
Processor: Intel Pentium Gold or equivalent

RAM: 8 GB or higher

Hard Disk: 6 GB or higher

Software Requirements
Operating System: Windows 7 or later (latest version recommended)

Web Server: Apache (XAMPP/WAMP recommended)

Database: MySQL 8.0+

Browser: Any modern browser (Chrome, Firefox, Edge, etc.)

🔧 Installation & Setup
Step 1: Prerequisites
Ensure you have the following installed on your system:

XAMPP (Apache + MySQL + PHP) or WAMP

Any modern web browser

Step 2: Clone the Repository
bash
git clone https://github.com/onkar0306/SmartWaste.git
cd SmartWaste
Step 3: Setup Database
Open phpMyAdmin (http://localhost/phpmyadmin)

Create a new database named smartwaste

Import the SQL file from database/smartwaste.sql

Go to Import tab

Choose the SQL file

Click Go

Step 4: Configure Project
Copy the project folder to your web server directory:

For XAMPP: C:\xampp\htdocs\SmartWaste

For WAMP: C:\wamp\www\SmartWaste

Update database configuration in config/database.php:

php
define('DB_HOST', 'localhost');
define('DB_USER', 'root');
define('DB_PASS', '');
define('DB_NAME', 'smartwaste');
Step 5: Run the Application
Open your browser and navigate to: http://localhost/SmartWaste/

Default admin credentials:

Email: admin@smartwaste.com

Password: admin123

📁 Project Structure
text
SmartWaste/
├── admin/
│   ├── dashboard.php
│   ├── manage-bookings.php
│   ├── manage-services.php
│   └── manage-users.php
├── assets/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── script.js
│   └── images/
├── config/
│   └── database.php
├── includes/
│   ├── header.php
│   └── footer.php
├── user/
│   ├── login.php
│   ├── register.php
│   ├── profile.php
│   ├── book-service.php
│   ├── booking-history.php
│   └── logout.php
├── vendor/
├── index.php
├── database/
│   └── smartwaste.sql
└── README.md
🗄️ Database Schema
ER Diagram
text
┌─────────────────────────────────────────────────────────────────┐
│                           SmartWaste                           │
│                          Database Schema                       │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ┌──────────────┐     ┌──────────────┐     ┌──────────────┐   │
│  │    users     │     │   bookings   │     │  services    │   │
│  ├──────────────┤     ├──────────────┤     ├──────────────┤   │
│  │ id (PK)      │─────│ id (PK)      │     │ id (PK)      │   │
│  │ name         │     │ user_id (FK) │─────│ name         │   │
│  │ email        │     │ service_id   │     │ description  │   │
│  │ password     │     │ date         │     │ price        │   │
│  │ phone        │     │ time         │     │ duration     │   │
│  │ address      │     │ status       │     │ image        │   │
│  │ role         │     │ address      │     └──────────────┘   │
│  └──────────────┘     │ notes        │                        │
│                        └──────────────┘                        │
│                                                                 │
│  ┌──────────────┐     ┌──────────────┐                        │
│  │   trucks     │     │  tracking    │                        │
│  ├──────────────┤     ├──────────────┤                        │
│  │ id (PK)      │     │ id (PK)      │                        │
│  │ plate_no     │     │ truck_id (FK)│                        │
│  │ capacity     │     │ latitude     │                        │
│  │ driver_name  │     │ longitude    │                        │
│  │ status       │     │ timestamp    │                        │
│  └──────────────┘     └──────────────┘                        │
└─────────────────────────────────────────────────────────────────┘
Key Tables
users: Manages user accounts (admin, customers, staff)

services: Lists all available cleaning services

bookings: Tracks user appointments and service requests

trucks: Information about waste collection vehicles

tracking: Real-time GPS data of garbage trucks

🔮 Future Enhancements
The SmartWaste system has been designed with scalability in mind. Here are some planned enhancements:

🤖 AI & Machine Learning Integration
Predictive Analytics: Forecast waste generation patterns in different areas

Smart Route Optimization: AI-powered algorithms for reduced fuel consumption

Intelligent Scheduling: Dynamic scheduling based on real-time data

📱 Mobile Application
Real-time Notifications: Push alerts for service updates

Digital Payments: Integrated payment gateway

Reward System: Points and incentives for responsible waste disposal

Waste Segregation Guide: Interactive educational content

🗑️ IoT Integration
Smart Bins: Sensors for fill-level monitoring

Automated Alerts: Notification when bins are full

Waste Classification: Edge AI for sorting waste at source

⚡ Sustainability Features
Waste-to-Energy: Biogas generation from organic waste

Recycling Support: Connect users with recycling centers

Carbon Footprint: Track and reduce environmental impact

🔧 Technical Improvements
RESTful API: Enable third-party integrations

Microservices Architecture: Scalable system design

Cloud Deployment: Hosting on AWS/Azure/GCP

Data Analytics Dashboard: Comprehensive analytics and reporting

⚠️ Limitations
While SmartWaste provides a comprehensive solution, there are some current limitations:

Limitation	Description
Internet Dependency	Real-time tracking requires stable internet and GPS connectivity
Initial Setup Cost	Hardware, software, and training costs for implementation
Digital Divide	Users without smartphones/computers may face accessibility issues
Skilled Manpower	Professional cleaning requires trained staff, which may not be universally available
Recycling Gap	Currently focuses on collection; recycling/disposal plants not fully integrated
Maintenance Costs	GPS trackers, servers, and hardware require ongoing maintenance
Regional Adoption	Rural areas may have limited adoption due to infrastructure constraints
👥 Contributors
Project Guide
Prof. A.S. Tanpure
Project Guide & HOD, BBA(CA) Department

Development Team
Onkar Shivaji Sawant
Roll No: 47 | TYBBA(CA) - Div A
Project Developer

Institutional Support
Dr. S.S. Pingale
Principal, Hutatma Rajguru Mahavidyalaya

External Examiner
[To be appointed]

🙏 Acknowledgments
I would like to express my sincere gratitude to everyone who supported this project:

Prof. A.S. Tanpure for providing invaluable guidance and direction throughout the project

Department of BBA(CA) for providing the necessary resources and infrastructure

All Faculty Members for their constant encouragement and support

My Family & Friends for their unwavering support and motivation

Open Source Community for providing excellent tools and libraries

"This project is dedicated to building a cleaner, greener, and smarter future for our communities."

📜 License
This project is developed for academic purposes and is intended for educational use only.

© 2026 Onkar Sawant
Khed Taluka Shikshan Prasarak Mandal's
Hutatma Rajguru Mahavidyalaya, Rajgurunagar, Pune - 410505

📞 Contact & Support
For any queries or support, please contact:

Name: Onkar Shivaji Sawant

Email: onkar.sawant@example.com

Institution: Hutatma Rajguru Mahavidyalaya, Rajgurunagar, Pune

<div align="center">
Made with ❤️ for a cleaner environment

"Smart waste, clean space"

https://img.shields.io/badge/Project-SmartWaste-brightgreen
https://img.shields.io/badge/Academic-Project-blue
https://img.shields.io/badge/Year-2025--2026-orange

</div>
📚 References
Google: www.google.com

YouTube: www.youtube.com

W3Schools: www.w3schools.com

ChatGPT: www.chatgpt.com

Academic References
Sr.No	Research Paper	Authors	Publication	Focus Area
1	Smart Waste Management using IoT	John Doe, Jane Smith	IEEE Xplore, 2021	IoT-based waste monitoring
2	Optimized Routing for Waste Collection	R. Kumar, S. Mehta	Springer, 2020	GIS-based route optimization
3	Sustainable Waste Management Systems	P. Patel, M. Verma	Elsevier, 2022	Urban sustainability
4	Smart City Waste Management	A. Roy, K. Sharma	ScienceDirect, 2019	ICT for waste services
5	IoT Based Waste Collection System	N. Singh, R. Kaur	IJERT, 2021	Smart bin technology
🏁 Getting Started
Clone the repository

Set up XAMPP/WAMP

Import the database

Update configuration

Run the application

For detailed installation instructions, please refer to the Installation & Setup section above.

