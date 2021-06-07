
Reference: 
https://www.docker.com/blog/getting-started-with-docker-using-node-jspart-i/

Steps: 

1. Set up the test app & check the POST and GET Calls 

POST  - http://localhost:8000/test
{
	"msg": "testing"
}


Followed by - 
GET - http://localhost:8000/test



2. Create a Dockerfile 

3. Build your docker image 

docker build --tag node-docker .

4. Creating a new tag for the image
 docker tag node-docker:latest node-docker:v1.0.0

5. In order to remove a tag 
docker rmi node-docker:v1.0.0

6. Running Containers 
docker run -d -p 8000:8000 --name rest-server node-docker


Here - rest-server is name of container & we specify port 8000 for the container



7. Stop container 
docker stop rest-server


8. Restart Container
docker restart rest-server


