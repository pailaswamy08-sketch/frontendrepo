# SmartEnroll Full Stack Project

SmartEnroll is now a full-stack project with:

- React + Vite frontend
- Spring Boot backend
- SQL database (MySQL)

## Project Structure

- `src/` frontend code
- `backend/` Spring Boot API

## Backend Setup (Spring Boot + MySQL)

1. Create a MySQL database:

```sql
CREATE DATABASE smartenroll;
```

2. Default backend DB config is in `backend/src/main/resources/application.properties`:

- `DB_URL` default: `jdbc:mysql://localhost:3306/smartenroll?...`
- `DB_USERNAME` default: `root`
- `DB_PASSWORD` default: `root`

3. Run backend:

```bash
cd backend
./mvnw spring-boot:run
```

If `mvnw` is not available, use:

```bash
mvn spring-boot:run
```

Backend starts at `http://localhost:8080`.

## Frontend Setup (React)

From the project root:

```bash
npm install
npm run dev
```

Frontend starts at `http://localhost:5173`.

Vite proxy is configured so `/api/*` requests from frontend are routed to Spring Boot.

## API Endpoints

- `POST /api/auth/login`
- `POST /api/auth/signup`
- `GET /api/courses`
- `GET /api/students/{studentId}/enrollments`
- `POST /api/students/{studentId}/enrollments`
- `DELETE /api/students/{studentId}/enrollments/{courseId}`

## Demo Login

- Username: `student001`
- Password: `123456`
- Role: `student`
