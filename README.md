# Boss Machine

## Overview
Through a custom-built API, the Boss Machine empowers users to manage an array of minions, oversee groundbreaking million-dollar ideas, and streamline endless meetings that fill up an entrepreneur's calendar. Built with Node.js and Express, along with a custom middleware, this application showcases the power of a RESTful API to perform CRUD operations, offering a seamless backend support for managing resources efficiently. Whether you're plotting your next big venture or simply keeping your entrepreneurial endeavors in check, the Boss Machine is your go-to command center.

## Getting Started

### Prerequisites
- Node.js
- npm (Node Package Manager)

### Installation
1. Download the starting code for the project.
2. Unzip the downloaded folder to access the project files.
3. Open your terminal and navigate to the root project directory.
4. Install the project dependencies by running: **npm install**
5. Start the server with: **npm run start**

This command starts the server on port 4001 and will restart automatically whenever changes are made to `server.js` or any file in the `server/` folder.

### Viewing the Application
- Open `index.html` in a web browser. For the best experience, use Google Chrome (version 60 or later) or Firefox (version 55 or later).

## Implementation Details

### Server Setup
- The server uses `body-parser` middleware for body-parsing and `cors` for handling Cross-Origin Resource Sharing (CORS).
- The API routes are mounted at `/api` and serve as the entry point for all backend operations.

### API Routes
The API supports the following routes:

#### Minions
- `GET /api/minions`: Fetch all minions.
- `POST /api/minions`: Create a new minion.
- `GET /api/minions/:minionId`: Fetch a minion by ID.
- `PUT /api/minions/:minionId`: Update a minion by ID.
- `DELETE /api/minions/:minionId`: Delete a minion by ID.

#### Ideas
- `GET /api/ideas`: Fetch all ideas.
- `POST /api/ideas`: Create a new idea.
- `GET /api/ideas/:ideaId`: Fetch an idea by ID.
- `PUT /api/ideas/:ideaId`: Update an idea by ID.
- `DELETE /api/ideas/:ideaId`: Delete an idea by ID.

#### Meetings
- `GET /api/meetings`: Fetch all meetings.
- `POST /api/meetings`: Create a new meeting.
- `DELETE /api/meetings`: Delete all meetings.

### Database Interaction
The application uses a simple in-memory database with helper functions to interact with the data. The database is seeded with initial data every time the server restarts.

### Custom Middleware
- `checkMillionDollarIdea`: Ensures that any new or updated idea is worth at least one million dollars based on its `numWeeks` and `weeklyRevenue` properties.

## Testing
The project includes a suite of tests to verify the functionality of API endpoints and middleware. To run the tests:
1. Navigate to the project root in your terminal.
2. Install the testing dependencies (if you haven't already): **npm install**

3. Run the tests with: **npm run test**

## Contributing
Feel free to fork the repository and submit pull requests with any enhancements or bug fixes.

## License
This project is licensed under the MIT License - see the LICENSE.md file for details.




