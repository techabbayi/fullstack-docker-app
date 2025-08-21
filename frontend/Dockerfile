# Use Node.js 20 (LTS) instead of 18
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the frontend code
COPY . .

# Expose Vite's dev server port
EXPOSE 5173

# Start Vite dev server
CMD ["npm", "run", "dev", "--", "--host"]
