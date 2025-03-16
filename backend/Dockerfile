FROM node:latest

# Create a directory for the app
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all other source code to the container
COPY . .

# Build TypeScript project 
RUN npm run build

# Expose the correct port
EXPOSE 5000

# Run the compiled JavaScript server
CMD ["node", "dist/server.js"]
