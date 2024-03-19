FROM ubuntu

# Set the working directory inside the container
WORKDIR /app

# copy a script file to the container
COPY script.sh .

# Make the script executable
RUN chmod +x script.sh

# Run the script when the container starts
CMD ["./script.sh"]