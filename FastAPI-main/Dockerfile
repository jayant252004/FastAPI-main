# Set base image
FROM ubuntu:latest  

# Install Python and pip
RUN apt update && apt install -y python3 python3-pip python3-venv  

# Set the working directory
WORKDIR /app  

# Copy project files
COPY . /app/  

# Create and activate a virtual environment
RUN python3 -m venv venv && \
    . venv/bin/activate && \
    pip install --no-cache-dir -r requirements.txt  

# Expose FastAPI port
EXPOSE 8000  

# Run the application
CMD ["venv/bin/python", "main.py"]
