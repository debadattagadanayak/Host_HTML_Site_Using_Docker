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
