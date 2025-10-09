# 📚 Library Management System

[![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white)](https://expressjs.com/)
[![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)](https://reactjs.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)](https://www.prisma.io/)


A full-stack Library Management System built with **Node.js, Express.js, Prisma ORM, PostgreSQL,** and **React.js**, designed to manage **books, members, and book issuance records** efficiently.  
It provides **secure RESTful APIs** and a **dashboard UI** to track books pending for return.


## 🏛️ Overview

The **Library Management System (LMS)** simplifies library operations by offering:

- **CRUD APIs** for Members, Books, and Issuances (including deletion).  
- **API security** using API keys to prevent unauthorized access.  
- **Dashboard UI** for tracking members with books due for return.  
- **Sample data** for quick testing and demonstration.  

Ideal for small libraries or as a learning project for full-stack development.


## 🗃️ Database Model

The LMS has three main entities:

1. **Member** – Stores information about library members.  
2. **Book** – Contains details about books in the library.  
3. **Issuance** – Tracks which member borrowed which book and its return status.

Prisma is used as the **ORM** to simplify database access, migrations, and querying.


## 🚀 API Endpoints

<details>
<summary>👥 Member API</summary>

| Method | Endpoint       | Description                  |
|--------|----------------|------------------------------|
| GET    | `/member/{id}` | Fetch details of a member    |
| POST   | `/member`      | Add a new member             |
| PUT    | `/member/{id}` | Update member details        |
| DELETE | `/member/{id}` | Delete a member              |

</details>

<details>
<summary>📘 Book API</summary>

| Method | Endpoint       | Description                  |
|--------|----------------|------------------------------|
| GET    | `/book/{id}`   | Fetch details of a book      |
| POST   | `/book`        | Add a new book               |
| PUT    | `/book/{id}`   | Update book information      |
| DELETE | `/book/{id}`   | Delete a book                |

</details>

<details>
<summary>📦 Issuance API</summary>

| Method | Endpoint        | Description                  |
|--------|-----------------|------------------------------|
| GET    | `/issuance/{id}`| Get details of a specific issuance |
| POST   | `/issuance`     | Issue a book to a member     |
| PUT    | `/issuance/{id}`| Update issuance details      |
| DELETE | `/issuance/{id}`| Delete an issuance record    |

</details>

## 🛠️ Technologies Used

| Layer          | Technology           |
|----------------|-------------------|
| Backend        | Node.js, Express.js |
| Database       | PostgreSQL          |
| Frontend       | React.js            |
| Authentication | API Keys            |


## ⚙️ Setup Instructions

### Backend Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/library-management-system.git

   cd library-management-system/backend
    ```

2. **Install dependencies**

    ```bash
    npm install
    ```

3. **Configure environment variables**

    Create a .env file in the backend root:

    ```bash
    DATABASE_URL=postgresql://username:password@localhost:5432/library_db
    API_KEY=your_secret_api_key
    PORT=5000
    ```

4. **Run database migrations**

    ```bash
    npx prisma migrate dev
    ```

5. **Start the backend server**

    ```bash
    node server
    ```

    Server runs at http://localhost:5004.

### Frontend Setup

1. **Navigate to frontend folder**

    ```bash
    cd ../frontend
    ```

2. **Install dependencies**

    ```bash
    npm install
    ```

3. **Start the frontend server**

    ```bash
    npm run dev
    ```

    Dashboard runs at http://localhost:3000.

## 🧪 Sample Data

- Members: John Doe, Jane Smith

- Books: “To Kill a Mockingbird”, “1984”

- Issuances: Sample issued books with due dates

## 🚧 Future Enhancements

- 🗑️ Soft delete for entities.

- 🔐 Role-based access control.

- 📧 Email notifications for due books.

- 📈 Analytics dashboard for book issuance trends.

## 👩🏻‍💻 Author

**Your Name**  

📧 [poshikamanivannan@gmail.com](mailto:your.email@example.com)  

🌐 [GitHub](https://github.com/PoshikaM)
