# Use the official Maven runtime with JDK 17 as a base image

# Set the working directory inside the container

# Copy the project files

# Expose the port that the application listens on

## 5. Define the command to run when the container starts.

# Stage 1: The Build Stage 🏗️
FROM eclipse-temurin:21-jdk-jammy AS build

# Set the working directory inside the container.
WORKDIR /app

# Copy the Maven project files from the root of your project to the working directory.
COPY . /app


# Use the Maven wrapper to package the application.
RUN ls -la .
RUN chmod +x ./mvnw
RUN ./mvnw clean package


# -----------------------------------------------------------------------------
# Stage 2: The Final Runtime Stage 🚀
FROM eclipse-temurin:21-jre-jammy

# Set the working directory for the final image.
WORKDIR /app

# Copy the final JAR file from the 'build' stage into this new image.
COPY --from=build /app/target/*.jar app.jar


# Document the port the application will run on.
EXPOSE 9090

# Define the command to run the executable JAR when the container starts.
ENTRYPOINT ["java", "-jar", "app.jar"]