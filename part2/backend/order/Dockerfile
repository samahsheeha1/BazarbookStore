# Use an OpenJDK base image
FROM openjdk:11-jre-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the compiled .jar file into the container
COPY target/OrderService.jar OrderService.jar

# Copy orders.csv to /app in the container
COPY src/main/resources/orders.csv /app/orders.csv

# Expose the port the service listens on
EXPOSE 4568

# Run the service
CMD ["java", "-jar", "OrderService.jar"]
