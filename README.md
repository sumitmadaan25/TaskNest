# TaskNest

A modern task management application built with React frontend and Spring Boot backend.

## 📋 Overview

TaskNest is a full-stack todo application that helps you organize and manage your tasks efficiently. The application features a responsive React frontend powered by Vite and a robust Spring Boot REST API backend with PostgreSQL database integration.

## 🛠️ Tech Stack

### Frontend
- **React 19.1.0** - Modern React with latest features
- **Vite 6.3.5** - Fast build tool and dev server
- **Axios 1.10.0** - HTTP client for API calls
- **React Icons 5.5.0** - Icon library
- **ESLint** - Code linting and formatting

### Backend
- **Spring Boot 3.5.3** - Java framework
- **Spring Data JPA** - Data persistence layer
- **PostgreSQL** - Primary database
- **Lombok** - Reduce boilerplate code
- **Java 21** - Latest LTS Java version
- **Maven** - Dependency management

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed on your system:

- **Java 21** or higher
- **Node.js 18** or higher
- **npm** or **yarn**
- **PostgreSQL** database
- **Maven 3.6+**

### Database Setup

1. Install and start PostgreSQL
2. Create a new database for the application:
```sql
CREATE DATABASE tasknest;
-- OR if you prefer to keep your existing database name:
-- CREATE DATABASE "ToDo_app";
```

3. Create a user (optional but recommended):
```sql
CREATE USER tasknest_user WITH PASSWORD 'your_password';
GRANT ALL PRIVILEGES ON DATABASE tasknest TO tasknest_user;
```

### Backend Setup

1. Navigate to the backend directory:
```bash
cd "TaskNest Backend"
```

2. Set up environment variables by creating a `.env` file in the backend directory or set system environment variables:
```bash
DB_NAME=ToDo_app
DB_USERNAME=postgres
DB_PASSWORD=your_actual_password
```

Alternatively, you can create `src/main/resources/application-local.properties`:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/ToDo_app
spring.datasource.username=postgres
spring.datasource.password=your_actual_password
```

3. Install dependencies and run:
```bash
mvn clean install
mvn spring-boot:run
```

The backend API will be available at `http://localhost:8080`

### Frontend Setup

1. Navigate to the frontend directory:
```bash
cd "TaskNest Frontend"
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

The frontend will be available at `http://localhost:5173`

## 📁 Project Structure

```
TaskNest/
├── TaskNest Frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── utils/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── public/
│   ├── package.json
│   └── vite.config.js
├── TaskNest Backend/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/project/
│   │   │   │   ├── controller/
│   │   │   │   ├── model/
│   │   │   │   ├── repository/
│   │   │   │   ├── service/
│   │   │   │   └── TaskNestApplication.java
│   │   │   └── resources/
│   │   │       └── application.properties
│   │   └── test/
│   └── pom.xml
├── README.md
├── LICENSE
└── .gitignore
```

## 🛠️ Available Scripts

### Frontend Scripts
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

### Backend Scripts
- `mvn spring-boot:run` - Start the Spring Boot application
- `mvn clean install` - Clean and install dependencies
- `mvn test` - Run tests
- `mvn clean package` - Package the application

## 🔌 API Endpoints

The backend provides RESTful APIs for task management:

- `GET /api/tasks` - Get all tasks
- `POST /api/tasks` - Create a new task
- `GET /api/tasks/{id}` - Get task by ID
- `PUT /api/tasks/{id}` - Update task
- `DELETE /api/tasks/{id}` - Delete task

## 🌐 Environment Variables

### Backend
Create `src/main/resources/application-dev.properties` for development:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/tasknest
spring.datasource.username=${DB_USERNAME:tasknest_user}
spring.datasource.password=${DB_PASSWORD:your_password}
```

### Frontend
Create `.env` file in frontend directory:
```env
VITE_API_BASE_URL=http://localhost:8080/api
```

## 🚀 Deployment

### Backend Deployment
1. Build the JAR file:
```bash
mvn clean package
```

2. Run the JAR file:
```bash
java -jar target/TaskNest-Backend-0.0.1-SNAPSHOT.jar
```

### Frontend Deployment
1. Build for production:
```bash
npm run build
```

2. Deploy the `dist` folder to your web server

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🐛 Issues

If you encounter any issues or have suggestions, please file an issue on the GitHub repository.

## 📞 Support

For support and questions, please open an issue in the GitHub repository.
