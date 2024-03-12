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


![1](https://github.com/CiutacuClaudia/DevOpsTasks/assets/93795693/ab439627-cc85-45ca-ac42-d9590bd418ed)
![1 2](https://github.com/CiutacuClaudia/DevOpsTasks/assets/93795693/052286dc-b4c7-4623-9993-d434bad9ba7f)
![1 1](https://github.com/CiutacuClaudia/DevOpsTasks/assets/93795693/7612b266-ed3e-4f20-b390-b63ef813fb19)
