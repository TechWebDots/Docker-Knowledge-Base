# Docker-Knowledge-Base
Docker-Knowledge-Base for hands-on examples
# To create a "Hello World" Docker image using a Dockerfile, follow these steps: 
## 1. Create a Dockerfile- Create a new file named Dockerfile (without any extension) in an empty directory. 
    ### Use a lightweight base image
    FROM alpine:latest

    ### Set the command to execute when the container starts
    CMD ["echo", "Hello World from Docker!"]

  1. FROM alpine:latest: This instruction specifies the base image for your Docker image. alpine:latest is a very small and efficient Linux distribution, making it a good choice for minimal images.
  2. CMD ["echo", "Hello World from Docker!"]: This instruction defines the default command that will be executed when a container is launched from this image. In this case, it will simply print "Hello World from Docker!" to the console. 

## 2. Build the Docker Image- Navigate to the directory containing your Dockerfile in your terminal and execute the following command: 
    docker build -t hello-world-image .

1. docker build: This command initiates the image building process. 
2. -t hello-world-image: This flag tags your image with a name (hello-world-image) for easy identification. You can choose any name you prefer. 
3. .: This indicates the build context, which is the current directory where your Dockerfile resides. 

## 3. Run the Docker Container- Once the image is built, you can run a container from it using: 
    docker run hello-world-image

This command will create and start a new container based on your hello-world-image, and you will see "Hello World from Docker!" printed to your terminal. 

