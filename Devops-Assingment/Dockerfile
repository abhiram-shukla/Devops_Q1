FROM python:3.12.4-slim

# Set environment variables to ensure the Python output is sent straight to the terminal (without buffering)
ENV PYTHONUNBUFFERED=1

# Set the working directory inside the Docker container
WORKDIR /myapp

# Copy the requirements.txt file into the container at /app
COPY requirements.txt /myapp/

# Install the dependencies specified in requirements.txt
RUN pip install -r requirements.txt

# Copy the entire project directory into the container at /app
COPY . .

# Specify the command to run the tests when the container starts
CMD ["pytest"]
CMD ["pytest", "--junitxml=pytest.xml"]

