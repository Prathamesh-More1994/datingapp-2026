# **Dating App (ASP.NET Core + Angular)**

This project is a full-stack dating web application built using ASP.NET Core Web API and Angular. <br>
The main goal of this project was to learn how to design and build a real-world full-stack application using modern development practices such as authentication, real-time communication, pagination, filtering, and cloud deployment.<br>
The application allows users to create profiles, browse members, like profiles, and send real-time messages.<br>
The project is deployed to Azure App Service with CI/CD using GitHub Actions.<br>

## Screenshot / Demo
![Members](https://github.com/Prathamesh-More1994/datingapp-2026/blob/main/Screenshot%201.png)
![Message](https://github.com/Prathamesh-More1994/datingapp-2026/blob/main/Screenshot%202.png)

## __Tech Stack__
**Backend**
- ASP.NET Core Web API
- Entity Framework Core
- ASP.NET Core Identity
- Repository Pattern
- SignalR (real-time messaging)
- JWT Authentication

**Frontend**
- Angular
- TypeScript
- DaisyUI
- Tailwind CSS

**Database**
- SQL Database (via Entity Framework Core)

**DevOps / Deployment**
- Microsoft Azure App Service
- GitHub Actions (CI/CD pipeline)

## Features 
**Authentication & Security**
- User registration and login
- ASP.NET Core Identity integration
- JWT based authentication

**User Profiles**
- Create and update profiles
- Upload profile photos
- View other members

**Member Discovery**
- Profile likes system
- Member filtering
- Pagination for large datasets

**Messaging**
- Real-time chat using SignalR

**Architecture**
- Repository Pattern
- Clean API structure
- Angular SPA consuming REST APIs

**Deployment**
- Continuous deployment using GitHub Workflow
- Hosted on Azure App Service

**Running the Project Locally**
## 1. Clone the repository

```bash
git clone https://github.com/Prathamesh-More1994/datingapp-2026.git
cd datingapp-2026
```

## 2. Start the Database (Docker)
This project uses SQL Server running in Docker for the database.

Make sure Docker Desktop is running, then start the SQL Server container:
```bash
docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=Password@1" 
-p 1433:1433 --name datingapp-sql 
-d mcr.microsoft.com/mssql/server:2022-latest
```

Verify the container is running:

```bash
docker ps
```

## 3.Apply Database Migrations

Navigate to the API folder and update the database.
```bash
cd API 
dotnet ef database update 
```

This will create the required tables.

## 4. Run Backend (API)

```bash
cd API 
dotnet restore 
dotnet run 
```

The API will start on: <br>
https://localhost:5001

## 5. Run Frontend (Angular)

```bash
cd client
npm install 
ng serve 
```

Open in browser: <br>
http://localhost:4200

## Deployment

The application is deployed using GitHub Actions CI/CD pipeline. <br>
Deployment flow: <br>

GitHub Push -> GitHub Workflow -> Build & Publish -> Azure App Service 
<br>
This allows automatic deployment whenever new changes are pushed to the repository.

## What I Learned

Through this project I practiced:
- Building REST APIs with ASP.NET Core
- Implementing Identity authentication
- Structuring applications with Repository Pattern
- Creating real-time applications with SignalR
- Building modern UI using Angular and DaisyUI
- Implementing pagination and filtering
- Setting up CI/CD pipelines
- Deploying applications to Microsoft Azure
