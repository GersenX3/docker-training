## Base Image
FROM python:slim-trixie

## Work Directory
WORKDIR /app

## Copy source code
COPY . .

## Install requirements
RUN pip install -r /app/requirements.txt

## Expose container port
EXPOSE 5001

## Execute Application
CMD ["python", "app.py"]