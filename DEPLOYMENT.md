# Deployment Instructions for Housing Rental and Sales System

## Environment Configuration

Before deploying the housing rental and sales system, ensure the following environment variables are configured:

1. **DATABASE_URL**: The connection string for your database.
   - Format: `postgres://user:password@localhost:5432/mydatabase`

2. **REDIS_URL**: The connection URL for your Redis service.
   - Example: `redis://localhost:6379`

3. **JWT_SECRET**: A secret key for JWT authentication.
   - Example: `my_super_secret_key`

4. **API_KEY**: (if applicable) for any third-party services used by the system.

5. **NODE_ENV**: Set to `production` when deploying to production environment.

## Deployment Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Raranoia/huose.git
   cd huose
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Run Migrations**:
   Ensure your database is set up correctly and run migrations:
   ```bash
   npm run migrate
   ```

4. **Start the Application**:
   ```bash
   npm start
   ```

5. **Access the Application**:
   Open your browser and go to `http://localhost:3000`.
   
6. **Monitoring**:
   Set up monitoring for your application using tools like New Relic or similar.

## Notes
- Always ensure to backup your database before running migrations.
- Update your environment variables as necessary when deploying to different environments (staging, production).