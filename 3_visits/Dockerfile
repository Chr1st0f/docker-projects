# Specify base image
FROM node:alpine

# Use a work directory if does not exist it will be created 
WORKDIR /app

# Copy only necessary file to start npm
# If the images is rebuild when only the application is modified
# it will be quicker because all the steps are in the cache 
# ( just after copy )
COPY ./package.json ./

# Install some dependencies
RUN npm install

# Copy files ( application ) to container 
COPY . .

# Default command 
CMD ["npm", "start"]