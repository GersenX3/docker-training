# Use the official Python image as the base image
FROM python:slim-trixie
# Set the working directory inside the container
WORKDIR /app
# Copy the requirements file to the working directory
COPY . .
# Install the dependencies
RUN pip install -r requirements.txt
# Copy the Flask application to the working directory

# Expose the port that the Flask application listens on
EXPOSE 8000
# Run the Flask application when the container starts
CMD ["python", "server.py"]