# Use an official Node.js runtime as the base image
FROM node:14

# Create a non-root user
RUN adduser --disabled-password --gecos '' myuser

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install the project dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . .

# Expose the port your Node.js app will run on
EXPOSE 8070

# Define environment variables
ENV PORT=8070
ENV MONGODB_URL=mongodb+srv://berthutapea:zkZ0tg0H7yiScvO5@cluster0.jwcfbn8.mongodb.net/db_student?retryWrites=true&w=majority

# Switch to the non-root user
USER myuser

# Command to run your Node.js application
CMD ["node", "server.js"]
