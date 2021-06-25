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

###Note!!! 

To make a changes to the js file, you need to rebuild the image to copy the new updated source code
into a new image otherwise the changes wont be reflecated. Its importan to know how the images works in docker. Images
are baiscally locked onces you build them, everything in the images is read-only, so you need to rebuild the image to add the new changes
just type the command: ```docker build```
then you will get new image name and id, then u can run it like in step 3)
