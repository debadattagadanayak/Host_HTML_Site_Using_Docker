# STEPS: 

+ Create a directory for your project and navigate to it in the terminal.

+ Place your index.html file in the project directory.

+ Create a new file called Dockerfile (without any file extension) in the project directory.

+ Open the Dockerfile in a text editor and add the following content:

```
# Use an appropriate base image
FROM nginx:latest

# Copy your index.html file to the nginx HTML directory
COPY index.html /usr/share/nginx/html/
```

+ Save the Dockerfile.

+ Open the terminal and navigate to the project directory.

+ Build the Docker image by running the following command:

```
docker build -t my-web-app .
```

+ Once the image is built, you can run a container based on it using the following command:


```
docker run -d -p 80:80 my-web-app
```

+ Open a web browser and visit http://localhost to see your index.html file being served by the Docker container.
+ If you are using cloud instances then go to http://<public_ip_Of_the_instance>

***
## If you want to push the image to dockerhub follow these steps

+ First, make sure you have a Docker Hub account. If you don't have one, you can create an account at https://hub.docker.com/.

+ Open a terminal or command prompt and log in to Docker Hub using the docker login command. This command will prompt you to enter your Docker Hub username and password.
```
docker login
```

+ Enter your Docker Hub username and password when prompted. If the login is successful, you will see a "Login Succeeded" message.

+ Tag your Docker image with your Docker Hub username and the desired repository name. Use the following command:
```
docker tag <image_id> <dockerhub_username>/<repository_name>:<tag>
```

+ Push the tagged image to Docker Hub using the docker push command:
```
docker push <dockerhub_username>/<repository_name>
```
+ Docker will begin pushing the image to Docker Hub. This process may take some time, depending on the size of your image and your internet connection speed.

+ Once the push is complete, you can verify that your image is available on Docker Hub by visiting your Docker Hub repository page.
