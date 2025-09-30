# Use official Node.js LTS Alpine image
FROM node:18-alpine

# Set working directory inside container
WORKDIR /app

# Copy package.json and package-lock.json first for caching
COPY package*.json ./

# Install only production dependencies
RUN npm install --production

# Copy the rest of the backend code
COPY . .

# Expose backend port
EXPOSE 5000

# Set environment variable
ENV NODE_ENV=production

# Start the server
CMD ["node", "server.js"]
