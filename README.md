# ASP.NET Core Razor Pages – Auth System with Admin Dashboard

## 📌 Project Overview

This is a fully functional **Authentication System** built with **ASP.NET Core Razor Pages**.  
It includes **user registration, login, logout, role-based access (Admin/User)**, and a dedicated **Admin Dashboard** to manage users.

---

## 🔧 Technologies Used

- ASP.NET Core 8.0 (Razor Pages)
- Entity Framework Core
- Identity Framework (Default Identity)
- SQL Server (LocalDB)
- Bootstrap 5 + Bootstrap Icons

---

## 🚀 Features

### ✅ Authentication
- User Registration
- Secure Login / Logout
- Password Hashing
- Email-based login

### ✅ Role Management
- Admin/User Role Assignment
- Role-based access to pages
- Admin-only pages protected

### ✅ Admin Dashboard
- View Admin Panel if role is "Admin"
- Custom welcome message
- Easily extendable for:
  - User list
  - Role edit
  - Logs/stats

### ✅ UI & Design
- Bootstrap 5 styled layout
- Responsive navigation bar
- Role-based links in navbar (Login/Logout/Register/Admin Panel)

---

## 📁 Folder Structure

```
📦AuthSystem/
 ┣ 📂Pages/
 ┃ ┣ 📜Index.cshtml
 ┃ ┣ 📜Privacy.cshtml
 ┃ ┣ 📜Dashboard.cshtml
 ┃ ┗ 📜AdminDashboard.cshtml
 ┣ 📂Pages/Shared/
 ┃ ┣ 📜_Layout.cshtml
 ┃ ┣ 📜_ViewStart.cshtml
 ┗ 📜Program.cs
```

---

## 🛠️ Setup Instructions

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/AuthSystem.git
cd AuthSystem
```

2. **Update Connection String**

In `appsettings.json`:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=YOUR_SERVER;Database=AuthDB;Trusted_Connection=True;"
}
```

3. **Run Migrations**

```bash
dotnet ef migrations add Initial
dotnet ef database update
```

4. **Run the Project**

```bash
dotnet run
```

5. **Login**

- Create a new user
- Make it Admin via DB manually or via role seeding (already in Program.cs)

---

## 👥 Roles in Use

| Role   | Access Level                  |
|--------|-------------------------------|
| Admin  | Full access to Admin panel    |
| User   | Can access Dashboard only     |

---

## 🔐 Security Features

- Passwords hashed via Identity
- Role-based authorization
- Anti-forgery protection via Razor

---

## 📌 How to Add More

- Add user listing to AdminDashboard
- Create Edit/Delete actions
- Integrate profile page for logged-in users

---

## 🤝 Contribution

Feel free to fork and enhance this project. Suggestions and pull requests are welcome!

---

## 📧 Contact

Created by [Your Name]  
For queries, contact: **yourname@email.com**
