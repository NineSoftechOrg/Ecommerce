FROM openjdk:17-jdk-slim

# Set the working directory inside the container
WORKDIR /app

# Install Maven
RUN apt-get update && apt-get install -y maven && apt-get clean

# Copy the entire project to the working directory
COPY . .

# Run Maven to clean and package the application
RUN mvn clean package

# Expose the application's port (adjust according to your application)
EXPOSE 8084

# Specify the command to run the application (adjust the JAR name accordingly)
CMD ["java", "-jar", "target/Vendor-Service-0.0.1-SNAPSHOT.jar"]
