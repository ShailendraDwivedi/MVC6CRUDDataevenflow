# MVC6CRUDDataevenflow
ASP .NET Core MVC 6 Project Template. Everyone should be able to use this template to build a ASP .NET Core web app with SQL Server database and beautifully looking bootstrap Web Design Standard UI in code first, entity framework and repository patterns.
Key Functions
1.	Landing page default page no design.
2.	Cross-platform with responsive.
Getting Started
These instructions will give you the project up and running on your local machine for development and testing purposes. 
Prerequisites
•	Visual Studio 2022 
•	.NET 6.0 SDK
•	Microsoft.EntityFrameworkCore 7.0.11 
•	Microsoft.EntityFrameworkCore.SqlServer 7.0.11
•	Microsoft.EntityFrameworkCore.Design 7.0.11
•	Microsoft.EntityFrameworkCore.Tools 7.0.11
(These packages install from Manage Nuget package)
•	Bootstrap as per requirement in projects
Using the Template for a New Project
1.	Launch Visual Studio 2022 and create a new project. Use the "ASP.NET Core Web Application" template (C#). Use a unique name for the new project.
2.	In the "Create a new ASP.NET Core web application" window, select ".NET Core" and "ASP.NET Core 6.0" in the dropdown menus. Choose the "Empty" project type and Check the "Configure for HTTPS" box. Click "Create".
3.	Once the project has been created, close Visual Studio.
4.	Create new folder and name the folder (Data).
5.	Create new class in Data folder then name BaseEntity and create BaseEntity property in BaseEntity.cs file.
6.	Create new class file in Data folder then name Category and create category property in Category.cs file and inherit form baseentity.
7.	Create new class file in Data folder then name Product and create product property in Product.cs file inherit form baseentity.
8.	Create new class in Data folder then name ApplicationDBContext and create ApplicationDBContext property in ApplicationDBContext.cs file and inherit form DBContext then create constructor option base and add DB Set of Category and product file.
9.	Open Appsetting.json file add here connection string for database connection and name database and server name.
10.	 Open Program.cs file then add dependency of ApplicationDBContext connection string.
11.	All is completed then go in visual studio tools and open Nuget package manager then open Package manager console.
12.	In Package manager console select project then add for migration command (Add-migration “Migration Name”) then add migration completed the update database command (Update-database) then you check database created successfully.
13.	If you want to change any field name and datatype, then you can follow same instruction 12 only change migration name.
14.	 When database created then you create one folder name Repository.
15.	Under Repository folder create interface (IRepository) and class (Repository) then inherit from interface (IRepository) and create constructor of Repository class add ApplicationDBContext and add entity set then create CRUD method with Dbset entity.
16.	Open Program.cs file then add dependency of IRepository and Repository.
17.	Create Controller name CategoryController and create constructor of CategoryController and also use IRepository in CategoryController. Then create index, Add, Edit and delete Action method then get list of category, add category, edit category and delete category form database.
18.	After Action method then Add view for List and Create partial view for Add, edit and delete category.
19.	Create Controller name ProductController and create constructor of ProductController and also use IRepository in ProductController. Then create index, Add, Edit and delete Action method then get list of category, add category, edit category and delete category form database.
20.	After Action method then Add view for List and Create partial view for Add, edit and delete category.
21.	Then run project then you can see output then click category menu then you can see category list, click add button then open model popup then add category name and save it after then if you want to edit and delete then click on button. Same process in product.





