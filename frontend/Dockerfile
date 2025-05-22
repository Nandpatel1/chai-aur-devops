FROM node:22

# Set working directory
WORKDIR /frontend

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy app files
COPY . .

# Expose port
EXPOSE 5173

# Start in dev mode with nodemon
CMD ["npm", "run", "dev", "--", "--host"]