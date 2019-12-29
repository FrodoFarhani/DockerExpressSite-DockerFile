# DockerExpressSite-DockerFile

First of all we should have kitematic, we can download it. then login with our docker hub account.
Then download node image and run it there. After runing it successfully, click docker cli in the left bottom of the kitematic window. No we can run our coomands:

# Build image:

docker build -f DockerFile -t so0oshiance/node .

    -f: is the name of our docker file in source code
    -t: is tag name to finde it in docker images
    . : is the path of our source code we wanna create image from

# Run image

docker run -d -p 8080:3000 so0oshiance/node
  
 we run the image that we created

# Check if everything is correct

docker ps

    we should see our image is running here with our tag name and now we can test it in the browser

---

# To push your image into docker hub:

docker login

    - insert username and password of your docker hub

docker images

    - choose correct repository name from images

docker push [repository name for exp: so0oshiance/node]
