# pull official base image
FROM node:15.8.0-buster-slim

# set working directory
WORKDIR /code/webapp

# add `/app/node_modules/.bin` to $PATH
ENV PATH /code/webapp/node_modules/.bin:$PATH

# install app dependencies
COPY package.json /code/webapp/package.json
#COPY package-lock.json /code/webapp/package-lock.json
RUN npm install --silent
RUN npm install react-scripts@3.4.1 -g --silent

# add app
COPY . /code/webapp/

# start app
CMD ["npm", "start"]
