# 1. Use a Node.js base image
FROM node:16-alpine

# 2. Create and set the working directory
WORKDIR /app

# 3. Copy package.json and package-lock.json
COPY package*.json ./

# 4. Install dependencies
RUN npm install

# 5. Copy the rest of the application code
COPY . .

# 6. Expose port 3000 for the dev server
EXPOSE 3000

# 7. Start the development server
CMD ["npm", "start"]
