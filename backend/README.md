# Backend - Item Manager Lab Test

## Setup
1. Install Node.js 20.13 or newer.
2. Open a terminal inside the backend folder and run:
   ```bash
   npm install
   ```
3. Copy `.env.example` to `.env` and set `MONGO_URI` to a reachable MongoDB connection string.
4. Start the server:
   ```bash
   npm run dev
   ```
   The backend restarts automatically when source files change. To run without
   the file watcher, use `npm start`.

## API Endpoints
- `GET /api/items`
- `GET /api/items/:id`
- `POST /api/items`
- `PUT /api/items/:id`
- `DELETE /api/items/:id`

## Discount Percentage

Items include `discountPercentage`, a number from 0 to 100 (inclusive).
Create and update requests accept decimal values, for example
`"discountPercentage": 12.5`. New items without this field default to 0.
List and detail responses include the value. Existing items without a saved
discount display 0% in the frontend and start with 0 in the Edit Item form.
Updates validate the same range as creation; updates that omit this field
preserve the saved discount.
