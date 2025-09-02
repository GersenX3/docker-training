# Use the official Node.js image as the base image
FROM node:lts-trixie-slim
# Set the working directory inside the container
WORKDIR /app
# Copy the server code to the working directory
COPY . .
# Change to the server directory

# Install the server dependencies
RUN cd server && npm install --legacy-peer-deps && cd ..
# Change back to the app directory

# Copy the client code to the client directory

# Change to the client directory

# Install the client dependencies
RUN cd client && npm install --legacy-peer-deps && npm run build && cd ..
# Build the React application

# Change back to the app directory

# Copy the README file to the root directory

# Expose the port that the server listens on
EXPOSE 4000
# Run the Node.js server when the container starts
CMD ["node", "server/server.js"]