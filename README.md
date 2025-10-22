# 🧾 ClaimsPortal

**ClaimsPortal** is an ASP.NET Core MVC web application that allows **lecturers** to submit claims and **programme coordinators** to review, approve, or reject them.  
It includes secure file uploads, user role–based navigation, and a transparent claim-tracking system.

---

## 🚀 Features

### 👩‍🏫 Lecturer
- Submit new claims (hours worked, hourly rate, notes)
- Upload supporting documents (`.pdf`, `.docx`, `.xlsx`)
- View submitted claims with real-time status updates

### 👨‍💼 Coordinator
- View all pending claims
- Approve or reject claims with a reason
- Download and verify supporting documents

### 🧰 System
- Role-based authorization (Lecturer / Coordinator)
- Simple and responsive Bootstrap UI
- In-memory data store for claims and attachments
- Unit-tested logic using **xUnit**

---

## 🧪 Testing

To ensure reliability, this project includes **xUnit unit tests** for core features such as:
- Claim calculations  
- Default claim statuses  
- Lecturer association  
- File upload flag  
- Submission timestamps  

To run tests:
1. Open **Test Explorer** in Visual Studio  
2. Build the solution (`Ctrl + Shift + B`)  
3. Click **Run All Tests**

---

## ⚙️ Technologies Used

- **.NET 8.0**
- **ASP.NET Core MVC**
- **xUnit** for testing
- **Bootstrap 5** for UI
- **C#** and **Razor Views**

---

## 🗂️ Project Structure

