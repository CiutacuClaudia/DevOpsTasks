## Task 2

### Dockerized Java Application

This repository contains a Dockerized Java application that prints a greeting message based on the value of an environment variable.

### Prerequisites

Before running the Dockerized application, make sure you have Docker installed on your local machine. You can download and install Docker Desktop from [here](https://www.docker.com/products/docker-desktop).

### Building the Docker Image

1. Clone this repository to your local machine:

   ```bash
   git clone <repository_url>
   ```

2. Navigate to the directory containing the Dockerfile and Java source code:

   ```bash
   cd <repository_directory>
   ```

3. Build the Docker image using the following command:

   ```bash
   docker build -t my-java-app .
   ```

### Running the Docker Container

Once the Docker image is built, you can run a container based on that image.

```bash
docker run -e MY_ENV_VAR="World" my-java-app
```

This command runs a container using the `my-java-app` image. Replace `"World"` with any value you want for your environment variable. If the environment variable is not provided, it will default to `"User"`.

### Testing

To ensure that the Dockerized application functions correctly within the container, follow these steps:

1. Run the Docker container as described above.
2. Verify that the application prints the expected greeting message based on the provided environment variable value.

   For example, if you set `MY_ENV_VAR` to `"World"`, the output should be:

   ```
   Hello, World!
   ```


![2-2](https://github.com/CiutacuClaudia/DevOpsTasks/assets/93795693/24d648c2-d2bb-4c72-9a55-48f948751c48)
