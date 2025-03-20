# Use Python 3.12 slim image as base
FROM python:3.12-slim

# Set working directory
WORKDIR /workspaces/bikeshare/bike_sharing_api/app

# Copy and install dependencies
COPY requirements.txt .
COPY bikeshare_model-0.0.1-py3-none-any.whl .
RUN pip install -r requirements.txt

# Copy the entire application
COPY . .

# Expose port if using a web app (adjust if needed)
EXPOSE 8000

# Command to run the application (modify based on your app)
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
