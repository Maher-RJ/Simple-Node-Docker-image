# Simple-Node-Docker-image

## How to create the image and use it in the Container
1) Clone/open the project with your favorite ide or any terminal 

2) To create the custom image based on the Dockerfile. Type the below command in the terminal
```
docker build .
```

You will get image ID, In windows maybe u will get long image id.

3) Copy the id was generated and type the command below
```
docker run -p 4000:80 <id>
```

-p stand for publish, this allow us to tell docker on which local port, this internal docker conatiner specfic port which is ```EXPOSE 80``` in the Dockerfile we wrote, should be accessible, so in our exmaple the port is 4000:80.

4) Now can you open your browser and type ```localhost:4000```
