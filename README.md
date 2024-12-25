# Quiz App

This full-stack Quiz application is developed using **Next.js** for the [client-side](https://github.com/alfathrajif/quiz-app-nextjs-frontend/tree/60019cd1248e2b7b903ff6c2e5635476badb1095) and **NestJS** for the [server-side](https://github.com/alfathrajif/quiz-app-nestjs-backend/tree/92a13bdbf3532fe562fa9200c956b6176576a130), It includes an admin system to manage quizzes and user subscriptions.

## Features

- **Authentication**: Leverages JWT and Passport to implement secure login and registration, ensuring data protection and user identity verification.
- **Responsive Design**: Designed to deliver a seamless user experience across various devices, adapting to different screen sizes for optimal usability.
- **Manual Payment**: Enables users to complete payments manually, with clear instructions and verification processes for smooth transactions.
- **Admin Dashboard**: Offers a comprehensive dashboard for administrators to manage quizzes, monitor user activities, and oversee subscriptions efficiently.

## Technologies

- **Frontend**: Next.js with React and TypeScript, providing a modern, scalable UI framework.
- **Backend**: NestJS written in TypeScript, utilizing Prisma as the ORM for database interactions.
- **Database**: MySQL, a reliable relational database for structured data storage.
- **State Management**: React Context for global state and Zustand for simpler, scalable state management needs.
- **Authentication**: Secure authentication implemented with JWT, supported by cookies for session handling and added flexibility.

## 📷 Screenshots

![Landing Page](https://raw.githubusercontent.com/alfathrajif/quiz-app/refs/heads/main/docs/Kalkulus-Platform-tryout-dan-penjelasan-soal--12-25-2024_07_56_AM.png "Landing Page")

---

## Running on Local

### Prerequisites

- Node.js (v14.x or later)
- npm or yarn
- MySQL database
- Environment setup for both Next.js and NestJS projects

### Clone the Repository

You have to clone the client-side and server-side one by one.

```bash
git clone https://github.com/alfathrajif/quiz-app-nextjs-frontend.git
```

```bash
git clone https://github.com/alfathrajif/quiz-app-nestjs-backend.git
```

### Set Up Environment Variables

#### Install Frontend Dependencies (Next.js)

1. Navigate to the `client` folder (assumed structure for Next.js project).
2. Create a `.env.development.local` file with the following variables:

```bash
NODE_ENV=development
NEXT_PUBLIC_API_URL=http://localhost:3001
COOKIE_NAME=hroa0FzN4k_dev
```

#### Backend Setup (NestJS)

1. Go to the `server` folder (assumed structure for NestJS project).
2. Create a `.env.development.local` file with the following variables:

```bash
NODE_ENV=development.local
PORT=3001
DATABASE_URL="mysql://root:@localhost:3306/quiz_app_dev"
CLIENT_URL="http://localhost:3000"
JWT_EXPIRATION=10h
JWT_SECRET=52AB3DCB99B48798759A39CC8A221
COOKIE_NAME=hroa0FzN4k_dev
```

### Install Dependencies

#### Frontend

```bash
cd client # Make sure it's in the client folder

npm install
# or
yarn install
```

#### Backend

```bash
cd server # Make sure it's in the server folder

npm install
# or
yarn install
```

### Set Up Database (Prisma)

Run Prisma migrations to create the database tables.

```bash
npm run prisma:migrate:dev
```

Optionally, seed the database if there’s a seed file

```bash
npm run prisma:seed:dev
```

### Run the Application

#### Backend (NestJS)

In the `server` folder, start the backend server in development mode:

```bash
npm run start:dev
# or
yarn start:dev
```

#### Frontend (Next.js)

In the `client` folder, start the frontend app:

```bash
npm run dev
# or
yarn dev
```

### Access the Application

- **Frontend**: Visit `http://localhost:3000`:
- **Backend**: Visit `http://localhost:3001`:

## Additional Notes

- Ensure the database is running and accessible via the credentials in `.env.development.local`
- Both frontend and backend servers should be running concurrently for the application to work as expected.
