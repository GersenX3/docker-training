# Stage 1: The Build Stage 🏗️
FROM eclipse-temurin:21-jdk-jammy AS build

# Set the working directory inside the container.
WORKDIR /app/springboot-demo

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
WORKDIR /app/springboot-demo

# Copy the final JAR file from the 'build' stage into this new image.
COPY --from=build /app/springboot-demo/target/*.jar app.jar


# Document the port the application will run on.
EXPOSE 8080

# Define the command to run the executable JAR when the container starts.
ENTRYPOINT ["java", "-jar", "app.jar"]