# Use nginx as the base image
FROM nginx:latest

# Set the working directory in the container
WORKDIR /usr/share/nginx/html

# Copy the HTML files from your project into the container
COPY . .

# Use an entrypoint to replace environment variables and start nginx
# Assume there's a script `docker-entrypoint.sh` that configures WS_BACK_URL
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["nginx", "-g", "daemon off;"]
