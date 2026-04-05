# Stage 1: Build React app
FROM node:18 AS builder

WORKDIR /app

ARG REACT_APP_API_URL
ENV REACT_APP_API_URL=$REACT_APP_API_URL

COPY package*.json ./
RUN npm install

COPY . .

# Build the app
RUN npm run build

# Stage 2: Serve using Nginx
FROM nginx:alpine

# Copy build files to nginx
COPY --from=builder /app/build /usr/share/nginx/html

# Expose port
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]