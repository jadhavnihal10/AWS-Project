# Use official Node.js image
FROM node:16-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json files
COPY package*.json ./

# Install the application dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Expose port 4000 (or the port your Node.js app uses)
EXPOSE 4000

# Command to start the Node.js app
CMD ["node", "index.js"]
