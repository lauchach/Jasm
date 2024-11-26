# Places Management System API Tests

## Setup
1. First, seed the database by running:
```bash
node src/scripts/seedData.js
```

## API Endpoints Testing (cURL commands)

### 1. Get All Places
```bash
curl -X GET http://localhost:3000/api/places
```

### 2. Get All Reviews
```bash
curl -X GET http://localhost:3000/api/reviews
```

### 3. Add New Review
```bash
curl -X POST http://localhost:3000/api/reviews \
  -H "Content-Type: application/json" \
  -d '{
    "userId": "REPLACE_WITH_ACTUAL_USER_ID",
    "placeId": "REPLACE_WITH_ACTUAL_PLACE_ID",
    "rating": 5,
    "comment": "Excellent place!",
    "date": "2023-12-25T12:00:00.000Z"
  }'
```

### 4. Get Reviews by Place Type
```bash
curl -X GET http://localhost:3000/api/reviews/by-type/Park
```

### 5. View Reports Page
```bash
curl -X GET "http://localhost:3000/reports?month=12&year=2023"
```

## Testing Process:

1. Start the server:
```bash
npm run dev
```

2. Run the database seeder:
```bash
node src/scripts/seedData.js
```

3. Execute the cURL commands above to test each endpoint

4. For the POST request, you'll need to:
   - First get a user ID using the GET /api/places endpoint
   - Then get a place ID using the GET /api/reviews endpoint
   - Replace the IDs in the POST request body

5. View the reports page in your browser at:
   http://localhost:3000/reports