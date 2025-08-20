# Use Node base image
FROM node:14-alpine

# Set working directory
WORKDIR /app

# Copy package.json first
COPY package.json ./

# Install dependencies
RUN npm install

# Copy the rest of the frontend code
COPY . .

# Expose frontend port
EXPOSE 3000

# Start React dev server
CMD ["npm", "start"]
