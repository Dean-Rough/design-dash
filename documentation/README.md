# design-dash

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### Backend and Database
This application uses a Node.js backend with Express and a database (MongoDB/PostgreSQL) for data persistence and multi-user support. The backend provides API endpoints for CRUD operations on projects and handles user authentication.

### Setup Backend
```
cd backend
npm install
npm run start
```

### Environment Variables
Create a .env file in the backend directory with the following variables:
```
DATABASE_URL=your_database_connection_string
JWT_SECRET=your_jwt_secret
```

Replace the values with your actual database connection string and a secure random string for JWT signing.
