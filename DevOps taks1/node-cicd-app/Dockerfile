# Use Node.js LTS version
FROM node:18

# Set working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package*.json ./
RUN npm install

# Copy app source code
COPY . .

# Expose port (adjust to your app)
EXPOSE 3000

# Start the app
CMD ["node", "index.js"]
