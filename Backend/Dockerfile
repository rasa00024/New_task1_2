# Use the official Node.js image as a base image
FROM node:14

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy the package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install the application's dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose port 8070 for the backend app
EXPOSE 8070

# Specify the command to run when the container starts
CMD ["npm", "start"]
