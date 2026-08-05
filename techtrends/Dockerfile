# Use Python 3.8 base image
FROM python:3.9

# Set working directory in container
WORKDIR /app

# Copy all application files to the container
COPY . .

# Install dependencies defined in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Initialize the database with pre-defined posts
RUN python init_db.py

# Expose application port
EXPOSE 3111

# Command to execute at container start
CMD ["python", "app.py"]