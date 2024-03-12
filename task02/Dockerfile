# Use official OpenJDK image as the base image
FROM openjdk:11

# Set the working directory inside the container
WORKDIR /app

# Copy the Java source code into the container
COPY Main.java /app

# Compile the Java source code
RUN javac Main.java

# Define environment variable if needed
ENV MY_ENV_VAR=""

# Command to run the Java application
CMD ["java", "Main"]
