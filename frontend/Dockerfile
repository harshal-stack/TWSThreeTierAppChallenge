# Use the official Node.js 14 image as a base image
FROM node:14

RUN mkdir -p home/three_tier_app
# Set the working directory in the container

WORKDIR /home/three_tier_app

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install the application's dependencies inside the container
RUN npm install

# Copy the rest of the application code to the container
COPY  /var/lib/jenkins/workspace/three_tier_app/frontend  .

# Exposing Port to the container
EXPOSE 3001

# Specify the command to run when the container starts
CMD [ "npm", "start" ]
