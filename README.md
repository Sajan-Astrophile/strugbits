# Real-Time Chat Application

This project is a real-time chat application built using Node.js, MongoDB, Mongoose with authentication, chat functionality, search features, and security measures implemented.

## Features

### Authentication APIs

- User Registration (Signup)
- User Authentication (Login)
- Password encryption using bcrypt
- Session management

### Real-time Chat APIs

- Sending and receiving messages in real-time
- Storing chat messages in the database
- Implementing socket for real-time communication

### Chat List API

- API endpoint to fetch the list of chat conversations for a user

### Search Feature

- Search functionality for users and messages
- Display relevant results based on user input

### 'Delete for Me' Feature

- Allowing users to delete their own messages in the chat

### 'Delete for Everyone' Feature

- Allowing users to delete messages for everyone

### Error Handling
- Utilizes catchAsync middleware for handling asynchronous errors in controller functions.
- Global error handling middleware to handle errors and provide appropriate responses.

### Security Measures

- Protection against Cross-Site Scripting (XSS) attacks
- API rate limiting to protect against abuse and potential denial-of-service attacks

### MVC Architecture
- Follows the Model-View-Controller (MVC) architecture for a structured and modular codebase.
- Models: MongoDB models for user and chat data.
- Views: EJS templates for rendering the frontend views.
- Controllers: Contains controllers for handling different functionalities such as chat, user - authentication, and error handling.
- Routes: Express routes for handling different API endpoints.
- Middlewares: Contains middleware functions for authentication and authorization.

### Start the Server
- node server.js


## Usage

1. **User Registration**:
   - Access the registration page at `localhost:3000/register`.
   - Provide the required details and submit the form.
   - Upon successful registration, you will be redirected to the login page.

2. **User Authentication**:
   - Access the login page at `http://localhost:3000`. in the browser
   - For testing, use "pass1234" for all users.
   - Enter your credentials and submit the form.
   - Upon successful authentication, you will be redirected to the dashboard.

3. **Chatting**:
   - After logging in, you can start chatting with other users in real-time.
   - Use the feature to find specific users or messages.
   - After logging in, you can start chatting with other users in real-time.
   - Utilize the feature to locate specific users or messages.
   - Users can edit their messages and delete them.
   - The chat will load all messages when initiated.


## API Endpoints

### Chat List API

- **GET /api/chats/:userId**
  - Retrieves the list of chat conversations for a user.
  - Example: `http://localhost:3000/api/chats/65d4967811b47d293c51799c`

### Chat Delete for Everyone

- **DELETE /api/delete-chat-for-everyone/:id**
  - Deletes a chat message for everyone in the chat.
  - Example: `http://localhost:3000/api/delete-chat-for-everyone/chatID`

### Search Feature

- **GET /api/search?query=:query**
  - Searches for users and messages based on the provided query.
  - Example: `http://localhost:3000/api/search?query=hello`

## Technologies Used

- Node.js
- Express.js
- MongoDB
- Mongoose
- Socket.IO
- bcrypt
- Express Rate Limit
- Multer
- and More
