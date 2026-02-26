# Stage 1: Build the React application
FROM node:18.12.1-bullseye-slim AS build
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Stage 2: Serve the application with a simple HTTP server
FROM node:18.12.1-bullseye-slim
WORKDIR /usr/src/app
RUN npm install -g serve
COPY --from=build /usr/src/app/build ./build
EXPOSE 3000
CMD ["serve", "-s", "build", "-l", "3000"]
