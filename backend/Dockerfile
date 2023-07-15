# Use an official Node.js runtime as the base image
FROM node:14-alpine

# Set the working directory inside the container
WORKDIR /backend

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the backend files to the container
COPY . ./

# Expose a port to run the backend
EXPOSE 5000

# Define the command to start the backend
CMD ["node", "server.js"]