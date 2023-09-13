# Use an official Node.js runtime as the base image
FROM node:14

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install application dependencies
RUN npm install

# Copy the rest of the application code into the container
COPY . .

# Build the React app
RUN npm run build

# Expose port 80 for the React app
EXPOSE 80

# Use Nginx to serve the React app
FROM nginx:1.19
COPY --from=0 /usr/src/app/build /usr/share/nginx/html
