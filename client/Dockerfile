# Dockerfile for Nuxt.js Client
# Use official Node.js image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the Nuxt.js application
RUN npm run build

# Expose port 3000 for the Nuxt.js client
EXPOSE 3000

# Start the application
CMD ["npm", "run", "start"]
