# Ooru - 2D Metaverse Application

A modern metaverse application where people can hang out, built with React, Node.js, and WebSocket technology. This project follows a monorepo pattern to organize shared code and multiple applications which is creted using turbo repo cli.

![alt text](image.png)

## Project Structure

```
OORU-APP/
├── apps/
│   ├── frontend/     # React + Vite metaverse client
│   ├── http/        # REST API server
│   └── ws/          # WebSocket server
├── packages/        # Shared code/libraries
└── tests/          # Test files
```

## Features

- **Virtual Space**: A metaverse environment for users to interact
- **Real-time Communication**: WebSocket implementation for live updates
- **Modern Frontend**: Built with React and Vite
- **Robust Backend**: REST API endpoints and WebSocket server
- **Database Integration**: PostgreSQL with Prisma ORM


## Upcoming Features

- Live Chat functionality
- Video Chat implementation
- More interactive elements

## Prerequisites

- Node.js
- npm
- PostgreSQL

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd OORU-APP
```

2. Setup database:
   - Create a `.env` file in `packages/db/`
   - Add your database URL:
   ```
   DATABASE_URL="postgresql://user:password@localhost:5432/db_name"
   ```
   - Navigate to the db package:
   ```bash
   cd packages/db
   ```
   - Generate Prisma client:
   ```bash
   npx prisma generate
   ```
   - Push the database schema:
   ```bash
   npx prisma db push
   ```
   - (Optional) Seed the database if you have seed data:
   ```bash
   npx prisma db seed
   ```
   - (Optional) To view your database using Prisma Studio:
   ```bash
   npx prisma studio
   ```

3. Install dependencies for all applications:
```bash
# In the root directory
npm install
```

4. Start the development servers:
```bash
# Start each application (run these in separate terminals)
cd apps/frontend && npm run dev
cd apps/http && npm run dev
cd apps/ws && npm run dev
```

## Running Tests

The project uses a comprehensive testing suite to ensure functionality across all components.

### Setting Up Test Environment

1. Install test dependencies:
```bash
cd tests
npm install
```
### Running Tests

```bash
# Run all tests
npm test

# Run tests with coverage report
npm run test:coverage

# Run tests in watch mode during development
npm run test:watch
```


## Project Components

### Frontend (`apps/frontend`)
- React-based client application
- Built with Vite for optimal development experience
- Handles the metaverse user interface and interactions

### HTTP Server (`apps/http`)
- REST API endpoints
- Handles authentication and data operations
- Communicates with the database

### WebSocket Server (`apps/ws`)
- Manages real-time communications
- Handles live updates and user interactions
- Enables real-time metaverse experience

### Shared Packages (`packages/`)
- Common utilities and configurations
- Database schemas and models
- Shared types and interfaces

## Technologies Used

- React
- Node.js
- WebSocket
- PostgreSQL
- Prisma ORM
- Vite

## Credits

This project was initially built following a tutorial by Harkirat Singh. You can find the tutorial [here](https://www.youtube.com/watch?v=aamk2isgLRk).

## Development

This is an active project with ongoing development. Future updates will include enhanced chat features and video communication capabilities. As of now this is just a base to be developed upon.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

[Add your license here]