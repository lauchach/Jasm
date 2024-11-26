# Places Management System

## Setup Instructions

1. Create a MongoDB Atlas account and get your connection string
2. Replace the `MONGODB_URI` in `.env` with your MongoDB Atlas connection string
3. Install dependencies: `npm install`
4. Seed the database: `node src/scripts/seedData.js`
5. Start the server: `npm run dev`

## Environment Variables

Create a `.env` file in the root directory with:

```
MONGODB_URI=your_mongodb_atlas_connection_string
```

Replace `your_mongodb_atlas_connection_string` with your actual MongoDB Atlas connection URL.

## Available Scripts

- `npm run dev`: Start development server
- `npm start`: Start production server
- `node src/scripts/seedData.js`: Seed the database with sample data

## API Endpoints

See `postman_tests.md` for detailed API documentation and testing instructions.