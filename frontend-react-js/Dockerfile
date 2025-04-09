FROM node:20

ENV PORT=3000
ENV PATH="/frontend-react-js/node_modules/.bin:$PATH"

WORKDIR /frontend-react-js

# Copy package.json and package-lock.json first
COPY package*.json ./

# Install dependencies before copying other files
RUN npm install --force

# Now copy the rest of the app
COPY . .

EXPOSE ${PORT}

CMD ["npm", "start"]
