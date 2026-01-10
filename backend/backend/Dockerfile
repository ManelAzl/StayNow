# Backend Dockerfile for NestJS + Prisma
FROM node:20-alpine 

WORKDIR /usr/src/app

# Copy package files
COPY package*.json ./
COPY prisma ./prisma/

# Install dependencies
RUN npm ci

# Copy source code
COPY . .

# Generate Prisma client
RUN npx prisma generate

# Expose port
EXPOSE 3000

# Development command (hot reload)
CMD ["npm", "run", "start:dev"]


