FROM node:21

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json separately to leverage Docker layer caching
COPY . .

# Install dependencies
RUN npm i

# Copy necessary files for the application
COPY .env.sample .env.local
# COPY other_required_files ...

# Expose the port your app runs on
EXPOSE 5173

# Command to run the application
CMD ["npm", "run", "dev", "--","--host"]

