FROM node:17-alpine

# Install nodemon globally so we can use it in the CMD
RUN npm install -g nodemon

WORKDIR /app

# We only copy the package.json file to the container so we can run the npm install command and cache the dependencies
COPY package.json . 

RUN npm install

# We copy the rest of the files to the container
COPY . . 

EXPOSE 4000

CMD ["npm", "run", "dev"]
