# Use an official Python runtime as a parent image
FROM python:3.10-slim

# Prevent Python from writing pyc files to disc & enable output buffering
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Set working directory
WORKDIR /app

# Install dependencies
COPY requirements.txt .
RUN pip install --upgrade pip &&
    RUN pip install -r requirements.txt

# Copy project
COPY . .

# Expose port 8000 and run the application
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
