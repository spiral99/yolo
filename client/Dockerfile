# Use an official Node.js runtime as the base image
FROM node:14-alpine

# Set the working directory inside the container
WORKDIR /client

# Copy the package.json and package-lock.json files to the container
COPY . ./

# Install the dependencies
RUN npm install

# Copy the app files to the container
COPY . ./

# Expose a port to run the backend
EXPOSE 3000

# Define the command to start the backend
CMD ["npm", "start"]