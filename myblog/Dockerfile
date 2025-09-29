FROM node:17-alpine

WORKDIR /app

# copy package.json to the container, so we can run the npm install command and cache the dependencies
COPY package.json .

RUN npm install

# copy the rest of the files to the container
COPY . .

# required for docker desktop port mapping
EXPOSE 3000

CMD ["npm", "start"]
