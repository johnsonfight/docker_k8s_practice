# Use Python slim image
FROM python:3.9-slim

# Set the working directory
WORKDIR /app

# Copy the Python script
COPY BiosChangePasswordREDFISH.py /app

# Copy the requirements file first to leverage Docker caching for dependencies
COPY requirements.txt /app

# Install any required Python libraries
RUN pip install -r requirements.txt

# Command to run script with arguments passed in by Kubernetes
ENTRYPOINT ["python", "BiosChangePasswordREDFISH.py"]