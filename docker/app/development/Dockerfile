FROM node:alpine

# where our Next.js app will live
RUN mkdir -p /app

# Set /app as the working directory
WORKDIR /app

# Copy package.json and package-lock.json
# to the /app working directory
COPY ./app/package.json /app/package.json
COPY ./.env /app/.env

# Install dependencies in /app
RUN yarn install

# Copy the rest of our Next.js folder into /app
COPY ./app /app

EXPOSE 3001

# Run yarn dev, as we would via the command line 
CMD [ "yarn", "dev" ]