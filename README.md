# ChatTerm

A modern, secure web-based chat application that combines the flexibility of casual conversations with robust security features. The platform offers both authenticated user accounts and guest access, making it accessible for all users while maintaining high security standards.

## Features

- **Authentication System**
  - Full registration with email and password
  - Guest access with temporary username
  - Secure password hashing and storage
  - JWT-based authentication

- **Chat Features**
  - Real-time messaging using WebSocket
  - Server/Channel system similar to Discord
  - Private messaging between users
  - Friend management system
  - Online status indicators
  - Message history
  - File sharing capabilities
  - Message encryption (end-to-end)

- **Security Features**
  - End-to-end encryption for messages
  - HTTPS/SSL encryption
  - XSS protection
  - CSRF protection
  - Rate limiting
  - Input sanitization
  - Regular security audits
  - Two-factor authentication (2FA)

## Tech Stack

### Frontend
- React.js with TypeScript
- Redux for state management
- Material-UI for components
- Socket.io-client for real-time communication
- Styled-components for styling

### Backend
- Node.js with Express
- WebSocket server (Socket.io)
- TypeScript
- MongoDB for database
- Redis for caching

## Prerequisites

- Node.js (v14 or higher)
- MongoDB
- Redis (optional, for caching)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/chatterm.git
cd chatterm
```

2. Install dependencies:
```bash
npm run install-all
```

3. Create a `.env` file in the root directory with the following variables:
```env
# Server
PORT=5000
MONGODB_URI=mongodb://localhost:27017/chatterm
JWT_SECRET=your_jwt_secret
CLIENT_URL=http://localhost:3000

# Client
REACT_APP_SOCKET_URL=http://localhost:5000
```

4. Start the development servers:
```bash
npm start
```

This will start both the frontend (http://localhost:3000) and backend (http://localhost:5000) servers.

## Project Structure

```
chatterm/
├── client/                 # Frontend application
│   ├── public/            # Public assets
│   │   ├── src/
│   │   │   ├── components/    # React components
│   │   │   ├── pages/        # Page components
│   │   │   ├── hooks/        # Custom React hooks
│   │   │   ├── store/        # Redux store
│   │   │   ├── styles/       # Global styles
│   │   │   ├── utils/        # Utility functions
│   │   │   └── types/        # TypeScript types
│   │   └── tests/            # Frontend tests
│   │
│   ├── server/                # Backend application
│   │   ├── src/
│   │   │   ├── controllers/  # Route controllers
│   │   │   ├── models/       # Database models
│   │   │   ├── routes/       # API routes
│   │   │   ├── services/     # Business logic
│   │   │   ├── middleware/   # Custom middleware
│   │   │   ├── utils/        # Utility functions
│   │   │   └── config/       # Configuration files
│   │   └── tests/            # Backend tests
│   │
│   ├── shared/               # Shared code between frontend and backend
│   │   ├── constants/       # Shared constants
│   │   ├── types/          # Shared TypeScript types
│   │   └── utils/          # Shared utilities
│   │
│   └── docs/                # Documentation
│       ├── api/            # API documentation
│       ├── setup/          # Setup guides
│       └── security/       # Security documentation
```

## Development

### Running Tests
```bash
npm test
```

### Building for Production
```bash
npm run build
```

### Linting
```bash
npm run lint
```

## Security

- All passwords are hashed using bcrypt
- JWT tokens are used for authentication
- HTTPS is enforced
- Input validation is performed on both client and server
- Rate limiting is implemented
- XSS and CSRF protections are in place

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Material-UI for the component library
- Socket.io for real-time communication
- MongoDB for the database
- React and Redux for the frontend framework 
