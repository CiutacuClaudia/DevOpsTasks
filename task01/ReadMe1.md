## Task 1 
### README: Linux Container Setup and `/etc/passwd` Manipulation

#### Setting Up the Linux Container
1. **Install Docker Desktop**: Ensure Docker Desktop is installed on your system.
2. **Download Ubuntu Image**: Pull an Ubuntu image from Docker Hub using the command `docker pull ubuntu:<tag>`.
3. **Run the Container**: Start a container based on the downloaded image with the command:
   ```bash
   docker run -it --name my_linux_container ubuntu:<tag>
   ```

#### Inside the Container
1. **Create User and Run Script**: Inside the container, create a new user 'john', then copy the 'create_large_file.sh' script to the container and execute it.
   ```bash
   adduser john
   # Copy the script (create_large_file.sh) and execute it
   ```

#### Bash Script for `/etc/passwd` Manipulation
1. **Script Description**: This script reads the `/etc/passwd` file and performs various actions.
2. **Script Contents**: found in passwd_script.sh