# Use a lightweight Node image
FROM node:14-alpine

# Set working directory inside container
WORKDIR /app

# Copy package.json first (better for caching)
COPY package.json ./

# Install dependencies
RUN npm install

# Copy the rest of the backend code
COPY . .

# Expose backend port
EXPOSE 5000

# Start the backend app
CMD ["npm", "start"]
