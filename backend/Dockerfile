# Backend service image
FROM node:18-alpine AS base
WORKDIR /usr/src/app

# Install dependencies
COPY package.json package-lock.json* ./
RUN npm install --production

# Copy backend source
COPY . .

ENV NODE_ENV=production
EXPOSE 5000
CMD ["npm", "run", "start"]
