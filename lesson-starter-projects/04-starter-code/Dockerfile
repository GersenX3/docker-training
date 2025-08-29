# 1. Use an OpenJDK base image, as it includes the Java Runtime Environment (JRE).
FROM openjdk:26-slim-trixie

# 2. Set the working directory to organize files inside the container.
WORKDIR /app

# 3. Copy the pre-compiled .jar file into the working directory.
# This assumes your .jar file is in the same directory as your Dockerfile.
COPY JavaApp.jar .

# 4. Define the command to execute the .jar file when the container starts.
# The developer's note provided the exact command needed.
CMD ["java", "-jar", "JavaApp.jar"]