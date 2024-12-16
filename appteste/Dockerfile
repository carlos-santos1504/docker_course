FROM node:18-alpine
# Use the official Node.js 12 image

WORKDIR /app
# Set the working directory to /app

COPY package.json .
# Copy the current directory package.json file to the container at /app

# Install build tools

RUN yarn install --production
# Install dependencies

COPY . .
# Copy the current directory contents into the container at /app

CMD ["node","src/index.js"]
# Run the app

EXPOSE 3000 
# Your app binds to port 3000 so you'll use the EXPOSE instruction to have it mapped by the docker daemon