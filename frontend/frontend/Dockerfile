# Frontend Dockerfile for React + Vite
FROM node:20-alpine 

WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm ci

# Copy source code
COPY . .

# Expose port
EXPOSE 5173

# Development command (hot reload)
CMD ["npm", "run", "dev", "--", "--host"]

