# Pull the Node image from Docker Hub
FROM node:14-slim AS build

# Setting Working Directory
WORKDIR /usr/app

# Copying only package.json
COPY package*.json ./

# Install Dependencies
RUN npm install

# Copy rest of the code to container
COPY . .

RUN ENVIRONMENT=production npm run build

EXPOSE 3080

# Run the API on Nodemon
CMD ["npm", "run", "dev"]