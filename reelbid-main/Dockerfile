# Use Node 20 (required by Next.js 16)
FROM node:20-alpine

WORKDIR /usr/src/app

# Copy package files first (better caching)
COPY package*.json ./

RUN npm install

# Copy rest of files
COPY . .

# Build Next.js
RUN npm run build

EXPOSE 8080

CMD ["npm", "start"]
