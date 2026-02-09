# Backend API

Clean Node.js + Express backend setup with MongoDB.

## Features

- Express server
- MongoDB connection using Mongoose
- Environment configuration with dotenv
- CORS enabled
- Health check endpoint

## Folder Structure

```
backend/
 ├── src/
 │   ├── app.js              # Express app configuration
 │   ├── server.js           # Server entry point
 │   ├── config/
 │   │   └── db.js           # MongoDB connection
 │   └── routes/
 │       └── health.route.js # Health check route
 ├── package.json
 ├── .env.example            # Environment variables template
 └── .gitignore
```

## Setup

1. Install dependencies:
```bash
cd backend
npm install
```

2. Create `.env` file from `.env.example`:
```bash
cp .env.example .env
```

3. Update `.env` with your MongoDB URI:
```
PORT=5000
MONGO_URI=mongodb://localhost:27017/kbastralaya
```

## Running the Server

Development mode (with nodemon):
```bash
npm run dev
```

Production mode:
```bash
npm start
```

## API Endpoints

### Health Check
**GET** `/api/health`

Response:
```json
{
  "status": "success",
  "message": "API is running",
  "timestamp": "2026-02-09T04:23:35.157Z"
}
```

## Dependencies

- **express**: Web framework
- **mongoose**: MongoDB ODM
- **dotenv**: Environment configuration
- **cors**: Cross-Origin Resource Sharing
- **nodemon** (dev): Auto-restart on file changes
