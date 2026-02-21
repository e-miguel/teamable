# Teamable Demo Project
This project is a full-stack web application built as part of TechWorld with Nana The IT Fundamentals Course.
It demonstrates how a complete software project works — from frontend development to backend, database connection, testing, packaging, and deployment.

### 🚀 Project Overview

This application allows you to:

- Get a user profile from a database
- Update a user profile
- Store and retrieve data from MongoDB
- Run a backend server using Node.js and Express

The project follows the Software Development Life Cycle (SDLC):

1. Plan
2. Develop
3. Test
4. Package
5. Deploy

### 🛠 Technologies Used

Frontend:
- HTML
- CSS
- JavaScript
- Vue.js

Backend:
- Node.js
- Express.js

Database:
- MongoDB

Testing:
- Jest

Other Tools:
- Git
- npm
- Linux Server (for deployment)

### 📂 Project Structure (Important File)

```server.js```

This file:
- Creates an Express server
- Connects to MongoDB
- Provides API endpoints
- Serves the frontend from the ```/dist``` folder

### ⚙️ Environment Variables

The app uses environment variables:
- DB_USER
- DB_PASS
- DEV

#### Development Mode

If ```DEV=true```, the app connects to MongoDB locally:

```mongodb://127.0.0.1:27017```

#### Production Mode

If ```DEV``` is not set, it connects using credentials:

```mongodb://DB_USER:DB_PASS@127.0.0.1:27017?authSource=company_db```

### 📡 API Endpoints

#### 1️⃣ GET ```/get-profile```

Returns user profile data from MongoDB.

Example Response:

```
{
  "name": "John",
  "email": "john@email.com",
  "interests": ["coding", "music"]
}
```

#### 2️⃣ POST /update-profile

Updates user profile in the database.

Example Request Body:

```
{
  "name": "John",
  "email": "john@email.com",
  "interests": ["coding", "music"]
}
```

If payload is invalid, it returns:

```
{
  "error": "invalid payload. Couldn't update user profile data"
}
```

#### ▶️ How to Run the Project

1. Install Dependencies

```
npm install
```

2. Start MongoDB

```
127.0.0.1:27017
```

3. Set Development Mode

On Mac/Linux:

```
export DEV=true
```

On Windows (PowerShell):

```
setx DEV true
```

4. Start the Server

```
node server.js
```

Server will run on:

```
http://localhost:3000
```

### 🔐 Validation

The project uses custom validation functions:

- ```isInvalidEmail```
- ```isEmptyPayload```

These prevent invalid data from being stored in the database.

### 🎓 What I Learned From This Project

- How frontend and backend communicate
- How to build REST APIs
- How to connect Node.js to MongoDB
- How environment variables work
- How to structure a real-world project
- How deployment works on a Linux server

### 🖥 Deployment Highlights

- Created Ubuntu Linux server in the cloud
- Configured firewall & SSH access
- Installed Node.js & MongoDB
- Packaged the application
- Deployed and ran the app on port 3000
- Configured environment variables (DEV, DB_USER, DB_PASS)

### 🌍 Previous Live URL

```http://161.35.166.89:3000/```

#### Running app in browser

<img width="610" height="724" alt="image" src="https://github.com/user-attachments/assets/e5c7c2a2-562d-41f2-8910-4f8fd7873510" />

⚠️ The application was deployed to a cloud Ubuntu server, configured manually via SSH. MongoDB authentication and environment-based configuration were implemented for secure multi-environment deployment. The infrastructure was later destroyed to prevent unnecessary cloud costs.

#### SSH session into server

<img width="508" height="692" alt="image" src="https://github.com/user-attachments/assets/c799fe91-0c82-4321-bd6e-bab0a6faf00b" />

#### MongoDB connection logs

<img width="763" height="234" alt="image" src="https://github.com/user-attachments/assets/967c4a15-2b0a-41ab-a0f2-82370c0bbd40" />

### 👨‍💻 Author

#### Eugenio Miguel Mendoza

DevOps Engineer

Completed as part of the TechWorld with Nana IT Fundamentals Course
