# SurveyPortal
Overview

The SurveyPortal project is an ASP.NET MVC application designed to facilitate surveys, with features for user registration, login, survey questions, responses, and data analysis tools for admin users. This README provides setup instructions, database configuration, and key details to help you run the application successfully.

Project Structure
TestApp.sln: The Visual Studio solution file for the SurveyPortal project.

TestApp: The main ASP.NET MVC project directory containing:

Program.cs: The entry point for the application.

appsettings.json: Configuration file for connection strings and app settings.

EmailSender.cs: Class handling email notifications within the application.

Database Backup: TestApp.bak, a backup of the SQL Server database.

Prerequisites
.NET Core SDK (version X.X or higher)
SQL Server for database management
Visual Studio 2019/2022 (or a compatible IDE)
SMTP server or email configuration for email functionality

Setup Instructions
1. Clone or Download the Repository
Unzip the project folder or clone the repository if available.

2. Database Setup
Restore the Database:

Open SQL Server Management Studio (SSMS).
Right-click on Databases > Restore Database...
Select Device and locate the TestApp.bak file found in the project folder.
Follow the prompts to restore the database.
Update Connection String:

Open appsettings.json in the TestApp directory.
Update the "ConnectionStrings" section with your SQL Server connection details:
json
Copy code
"ConnectionStrings": {
    "DefaultConnection": "Server=YOUR_SERVER;Database=TestApp;User Id=YOUR_USERNAME;Password=YOUR_PASSWORD;"
}
3. Application Configuration
Configure Email (Optional, if email functionality is required):

In appsettings.json, add your SMTP settings under the "EmailSettings" section:
json
Copy code
"EmailSettings": {
    "Host": "smtp.your-email-provider.com",
    "Port": 587,
    "Username": "superadmin@gmail.com",
    "Password": "123Pa$$word!"
}

Build the Project:

Open the TestApp.sln file in Visual Studio.
Build the solution to restore NuGet packages and compile the project.

4. Run the Application
Set TestApp as the startup project.
Press F5 or click on Run to start the application.
Access the application at http://localhost:5000 or the specified local port.

Features
User Registration and Login: Allows users to register and log in to participate in surveys.

Admin Dashboard: Accessible only to admin users to manage surveys, view responses, and analyze data.

Email Notifications: Configurable for sending notifications related to surveys.

Troubleshooting
Database Connection Issues: Ensure SQL Server is running and that the connection string in appsettings.json is correctly configured.

Email Issues: Check SMTP settings and verify that your email provider allows SMTP access
