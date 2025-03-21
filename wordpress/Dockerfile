# Use the official WordPress image
FROM wordpress:latest

# Install necessary dependencies (optional, if needed)
RUN apt-get update && \
    apt-get install -y curl unzip && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Copy custom wp-config.php (if required)
COPY wp-config.php /var/www/html/wp-config.php

# Set the correct permissions
RUN chown -R www-data:www-data /var/www/html/wp-config.php

# Expose WordPress port
EXPOSE 80

# Start the default WordPress entrypoint
CMD ["apache2-foreground"]
