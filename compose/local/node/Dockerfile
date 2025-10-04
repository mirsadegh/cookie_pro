FROM node:20-alpine

WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm ci --only=production=false

# Copy project
COPY . .

# Default command
CMD ["npm", "run", "dev"]
