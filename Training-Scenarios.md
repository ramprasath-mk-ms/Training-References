25-05 15:29
-----------
Those who have completed the first two tasks, please inform me and start working on this new task.
 
 
Task 3 : 
 
```cs
public class Project
{
    public int Id { get; set; }
    public string Name { get; set; }
    public string Status { get; set; } // Active, Completed, On Hold
    public DateTime StartDate { get; set; }
    public int Budget { get; set; }

    // Static dataset for exercises
    private static List<Project> projects  = new List<Project>
    {
        new Project { Id = 1, Name = "AI Chatbot", Status = "Active", StartDate = new DateTime(2025, 1, 10), Budget = 50000 },
        new Project { Id = 2, Name = "Website Revamp", Status = "Completed", StartDate = new DateTime(2024, 11, 1), Budget = 20000 },
        new Project { Id = 3, Name = "Mobile App Development", Status = "Active", StartDate = new DateTime(2025, 3, 15), Budget = 75000 },
        new Project { Id = 4, Name = "Cloud Migration", Status = "On Hold", StartDate = new DateTime(2024, 6, 5), Budget = 40000 },
        new Project { Id = 5, Name = "ERP Upgrade", Status = "Completed", StartDate = new DateTime(2025, 2, 20), Budget = 120000 },
        new Project { Id = 6, Name = "IoT Device Integration", Status = "Active", StartDate = new DateTime(2025, 8, 1), Budget = 90000 },
        new Project { Id = 7, Name = "Data Warehouse", Status = "Active", StartDate = new DateTime(2025, 8, 25), Budget = 30000 }
    };
}
```

Instructions:
create method  of  GetAllProjects and use foreach for best practices 
All data should be in-memory (no database calls).
No LINQ — use loops and if conditions.
Create methods for each

1.Return the number of projects that are "Completed".
2.Return the name of the project with ID = 1.
3.Return the project to Check if any project has a budget greater than 1,00,000.
4.Return the names of projects starting next month
5.Return the count of projects where Status = "Active" and Budget is greater than 50,000.
6.Return the name of the project with the lowest budget, but only if Status is "Completed".
7.Return a single Project that has "Active" status and is starting next month.
8.Return the total budget of projects that start in the current month.
9.Return the average budget of "Completed" projects (manual calculation).
10.Return the number of projects grouped by Status, in this format:
"Active: X, Completed: Y, On Hold: Z".
11.Return all projects that have a StartDate between two given dates (parameters: fromDate, toDate).
12.Return true if all active projects have a budget greater than 30,000, otherwise false.
13.Return the count of projects where the name length is greater than 10 characters and Status is not "On Hold".
15.Return only the first three projects from the list
16.Return "Project Found" if a project exists with ID = 5, otherwise return "Not Found"
17.Return  only the months (in text, e.g., "January") of all project start dates


01-06 16:28
-----------
Everyone Freshers 
This is the CRUD application task assigned to you. Please work on it
 
 

Scenario
 
You are building a backend API for a small library. 
The library needs to manage its book inventory. 
You must design the database from C# classes and expose REST endpoints.
Requirements
Model — create these two entities:
Book
    Id (int, PK, auto-increment)
    Title (string, required, max 200 chars)
    Author (string, required, max 100 chars)
    ISBN (string, unique, max 20 chars)
    Price (decimal, required)
    StockCount (int, default 0)
    CategoryId (int, FK)
    CreatedAt (DateTime, auto set)
 
Category
    Id (int, PK)
    Name (string, required, max 100 chars)
    Books (navigation property ? List<Book>)
1.Use SQL Server as the database.
2.Create two separate projects:
     Implement the solution using:
        Code First Approach (Entity Framework Core Migrations)
        Database First Approach (Scaffold Existing Database)
3.Use Postman to test and execute all API endpoints.
4.Implement complete CRUD operations for all entities.
5.Follow the Repository Pattern for data access.
6.Implement proper logging for all CRUD operations.
7.Add Exception Handling and return meaningful API responses.
8.Maintain proper separation of concerns between Controller, Service, and Repository layers.
9.Use Dependency Injection throughout the application.
10.Write clean, maintainable, and optimized code following industry standards.
11.Optional: Create a custom middleware to log incoming requests, responses, execution time, and exceptions.


05-06 11:39
-----------
Customer Management System (CRUD)
 
Requirements
- Add a new customer
- View customer details
- Update customer information
- Delete customers (Soft Delete)
 
Database Design - Customer Table
CustomerId (PK), FirstName, LastName, Email, MobileNumber, DateOfBirth,
Address, IsActive, CreatedDate, UpdatedDate, DeletedDate
 
API Endpoints
1. Create Customer (POST /api/customers)
   - Validate required fields
   - Validate unique email and mobile number
Request:
{
        "firstName": "Manikandan",
        "lastName": "A",
        "email": "mani@test.com",
        "mobileNumber": "9876543210",
        "address": "Chennai"
      }
Validations:
First Name Required 
Last Name Required 
Mobile Number Required 
Email format validation 
Mobile number must be unique 
Email must be unique
							
2. Get Customer By Id (GET /api/customers/{id})
3. Get All Customers
4. Update Customer (PUT)
 
5. Soft Delete Customer (DELETE)
   - Set IsActive = 0 and DeletedDate
 
Business Rules
- Duplicate Mobile Number Not Allowed
- Duplicate Email Not Allowed
- Customer Age Must Be Greater Than 18
 
Expected Architecture
Controller
-> Service Layer
-> Repository Layer
-> Entity Framework Core
-> SQL Server


11-06 12:07
-----------
Manikandan A anne 
Topics Covered in Yesterday's Class:(JWT Class)
Authentication and Authorization
Role-Based Authorization
Different Authentication and Authorization Methods
JSON Web Tokens (JWT)
JWT Structure and Claims
Token Handling and Management
Session Expiry and Timeout Mechanisms
Idle Timeout
Absolute Timeout
Password Encryption and Decryption & Password Hashing
Access Token Implementation & Refresh Token Implementation
Secure Session Management
 
Gowtham SK if I've missed any topics ,kindly mention it grp

17-06 13:28
-----------
Hi Manikandan A anne
Topics Covered in Today's ADO.NET Session
Introduction to Databases
Overview of ADO.NET
Need and Purpose of ADO.NET
.NET Family Overview
SqlConnection
SqlCommand
ExecuteNonQuery()
ExecuteReader()
SqlDataReader
ExecuteScalar()
SqlParameter
SqlDataAdapter
DataSet
DataTable
DataRow
CRUD Operations using ADO.NET (Create, Read, Update, Delete)


22-06 14:28
-----------
Hi Manikandan A anne Topics Covered in Today's Winforms Session
 
Introduction to .NET and C#
Overview of Windows Forms
Hands-On: Building a Simple Form
Understanding the Project Structure
Exploring Windows Forms Controls
Working with Control Properties
Understanding Event-Driven Programming(explained Event Flow)
Commonly Used Events
Form Events
Button Events
TextBox Events
ComboBox Events
Database Fundamentals
Real-World Application Architecture


22-06 15:19
-----------:
Employee Registration Form
==================== 
 
Name*
Email*
Mobile Number*
Gender*
Address
 
Display success/failure message
Submit btn should show registered Successfully message
Validate mandatory(*) fields.



22-06 15:28
---
Employee Registration Form
Fields:
Name *
Email *
Mobile Number *
Gender *
Date of Birth
Department
Address
Controls:
TextBox
RadioButton
ComboBox
DateTimePicker
Button
Buttons:
Submit
Clear
Validation:
Mandatory field validation
Mobile Number: 10 digits only
Email format validation
Database:
Create Database: EmployeeDB
Create Employee table
Save employee details to SQL Server on Submit
Display success/failure message
Clear controls after successful save
Success Message:
"Employee Registered Successfully"
Failure Message:
"Employee Registration Failed"


25-06 13:28
-----------
Hi Manikandan A anne Topics Covered in Today's WebForms Session
 
Introduction to ASP.NET Web Forms
Advantages of ASP.NET Web Forms
Client-Server
ASP.NET Web Forms Project Structure(explained all detaily)
ASPX Page(HTML vs ASP.NET Controls ,runat="server",Server Controls,Control Properties)
Code Behind(Separation of UI and Business Logic,Event Handling)
Master Page
Server Controls(Basic Controls,Selection Controls,Data Controls,Navigation Controls)
ASP.NET Page Life Cycle(Page_Load,Page_Init)
PostBack(Why !IsPostBack is used with real time example)
State Management(ViewState,Session,Cookies)
Validation Controls



25-06 13:34
-----------
Develop an Employee Management System using ASP.NET Web Forms.
Requirements
Create an Employee form with the following fields:
Employee Name
Email
Mobile Number
Gender
Department
Date of Birth
Implement the following functionalities:
Create Employee
View Employee Details
Update Employee Details
Delete Employee Details
Additionally, implement the following State Management concepts:
Implement the following State Management concepts:
ViewState – Store the selected Employee ID while editing.
Session – Store and display the logged-in user's name.
Cookies – Store the last selected Department and load it when the page is reopened.
Use appropriate validation for all mandatory fields.
 
Deadline: Today EOD


30-06 13:34
-----------
Hi Manikandan A Anne,
Topics Covered in Today's ASP.NET MVC Session:
1. Introduction to ASP.NET MVC
2. Evolution of .NET
.NET Framework
.NET Core
.NET (5/6/7/8/9/10)
Brief explanation of the differences between each platform
3. MVC vs ASP.NET Web Forms
4. MVC Architecture
5. ASP.NET MVC Project Structure
6. MVC Components
Model
View
Controller
Action Methods
7. Routing
8. Partial Views
9. Filters
10. ViewBag, ViewData & TempData with examples
11. HTML Helpers


Develop an Employee Management System using ASP.NET MVC. 

Functional Requirements
Login Page
Employee Dashboard
Create Employee
View Employee Details
Update Employee Details
Delete Employee Details
Logout

Employee Details
Employee Name
Email
Mobile Number
Gender
Department
Designation
Salary
Date of Joining

Note: Do not display the Employee ID on the Add or Edit page. The Employee ID should be auto-generated and used internally for Update and Delete operations.

Mandatory Requirements
Implement complete CRUD operations.
Apply Client-Side and Server-Side Validation.
Use appropriate Data Annotations for validation.
Use ViewBag and ViewData 
Display Success, Error, Update, and Delete messages using SweetAlert.
Display notifications using Toast Alerts.
Display employee records using jQuery DataTables (Search, Sorting, Paging).

Validation Requirements
Employee Name is mandatory.
Email must be in a valid format.
Mobile Number must contain exactly 10 digits.
Department is mandatory.
Designation is mandatory.
Salary should accept only numeric values.
Date of Joining is mandatory.


08-07 15:21
-----------
Image Upload Requirements:
Upload a Profile Image while creating a new employee.
Store the uploaded image in the Uploads folder.
Save only the image path in the SQL Server database.
Display the uploaded profile image in:
    Employee List
    Employee Details Page
    Edit Employee Page
While editing, if a new profile image is uploaded, replace the existing image with the new one.
If no profile image is available, display a default profile image.

Image Validation Requirements:
Profile Image is mandatory while creating a new employee.
Allow only the following file formats:
    .jpg
    .jpeg
    .png
Maximum allowed file size: 2 MB.
Display an appropriate validation message for:
    Invalid file format.
    File size exceeding 2 MB.
Do not allow duplicate file names while saving images (generate a unique file name before storing the image).


16-07 10:56
-----------
Task Overview

An Excel file will be available in a specific location. At a scheduled time, the application should:
    Read the Excel file.
    Check whether there is any new or updated data.
    If a new employee record is found, insert it into the database.
    If an existing employee record has changed, update the corresponding record in the database.
    Whenever a new employee is added, send a welcome/notification email to that employee.
 
Before starting the implementation, please understand:
    The basic concept of Cron Jobs.
    Background Services in .NET.
    Different types of background jobs (e.g., BackgroundService, IHostedService, Hangfire, Quartz.NET, Windows Service, etc.) and when to use them.

Once you have a clear understanding of the concepts, start implementing the task.
If you have any questions or need clarification on the requirements, please let me know.Thanks


23-07 13:35
-----------
Hi Jagadhesh M Muthuprabhu B Ramprasath K, if you are learning Microservices architecture, API Gateway, Kafka, and Redis, you can refer to this code. It is implemented using .NET 10 with an API Gateway, production-level Kafka architecture, and Redis integration.

https://github.com/Gowtham171811/Kafka_ApiGateway_Redis_Dotnet



24-07 17:20
-----------
https://newsdata.io/
 
Read the above documentation and try to implement the following APIs.
 
1. Search News
2. Top Headlines
3. Category News
4. News by Source

@freshers post an update in this channel as you complete each of the following steps
✅ Created a NewsAPI account
✅ Generated the API key
✅ Read the NewsAPI documentation
✅ Tested the APIs using Postman
Once all the above prerequisites are finished, you can start your implementation.


27-07 16:48
-----------
Task: Develop ASP.NET Core MVC Application

Requirements:
1. Create a Dashboard page with navigation to:
    Search News
    Top Headlines
    Category News
    News by Source
2. Consume the existing News API using HttpClient.
3. Display the API response in a clean and user-friendly UI.
4. Implement OAuth 2.0 / OpenID Connect (OIDC) authentication to secure the MVC application,Handle API errors gracefully (e.g., No Data Found, Server Error, Unauthorized).

Note: 
Do not implement any API logic. The MVC application should consume the existing News API endpoints only.
Ensure that access to the MVC application is secured using OAuth 2.0 / OpenID Connect, and only authenticated users can access the dashboard and news modules.








