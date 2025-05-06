## Deployed Application

You can access the deployed backend at the following URL:

[Phonebook Backend](https://phonebook-database-1.onrender.com) 
 
## Fullstack Open 2025 - Part 3

This repository contains the implementation of part 3 of the Fullstack Open course, focusing on building a phonebook application. The backend is built using Node.js and MongoDB, and RESTful APIs are implemented to manage phonebook data.


## 🧹 Lint Configuration (Exercise 3.22)

In this final step of Part 3, ESLint was added and configured to ensure consistent code style and detect potential bugs and bad practices in the codebase.

Start the application locally
To start an application:

# Install dependancies
$ npm install $

$ create a .env file and put there the MONGODB_URI for connecting to your mongodb database $
$ echo "MONGODB_URI=<YOUR-MONGODB-URI>" > .env $

# Start the application
$ npm run dev $

## This backend covers the following exercises:

- **3.1–3.6:** Basic Express server, JSON responses, route handling, and POST validation
- **3.7–3.8:** Logging with Morgan (including custom tokens for POST data)
- **3.9:** Connecting backend with the frontend from Part 2
- **3.10:** Deploying the backend to the web
- **3.11:** Serving the frontend from the backend (full stack integration)
# MongoDB Integration(Exercises 3.13–3.18)

 In these exercises, the backend is refactored to fully utilize **MongoDB** via **Mongoose** for data persistence. All interactions with phonebook data now occur through the database instead of in-memory arrays.

### ✅ 3.13 – Fetch All from MongoDB

- All GET requests to `/api/persons` now return data directly from the database.

### ✅ 3.14 – Save to MongoDB

- New contacts submitted via POST requests are saved to MongoDB.

### ✅ 3.15 – Delete from MongoDB

- DELETE requests to `/api/persons/:id` now remove the entry from the database.

### ✅ 3.16 – Centralized Error Handling

- All Mongoose-related and route-specific errors are now caught and processed by a centralized Express **error handler middleware**.

### ✅ 3.17 – Update Existing Contacts

- If the frontend detects a duplicate name, it issues a **PUT request** to update the contact’s number.
- The backend now supports `PUT /api/persons/:id` to update a contact's number in MongoDB.

### ✅ 3.18 – Database Integration for All Routes

- The following routes now work with MongoDB and return real-time data:
  - `GET /api/persons/:id` – fetches a single contact by ID
  - `GET /info` – displays total number of entries and current timestamp