## 1. Which base image do you want to use?
FROM python:slim-trixie

## 2. Set the working directory
WORKDIR /flask-demo

## 3. Copy the project files into the working directory.
COPY . .

## 4. Install the dependencies
RUN pip install -r requirements.txt

## 5. Document and inform the developer that the application will use PORT 5000 of the container.
EXPOSE 5000

## 6. Define the command to run when the container starts.
# ENV FLASK_APP=app.py
CMD ["python", "app.py"]
# CMD ["python", "app.py"]