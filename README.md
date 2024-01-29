# tamatem-task

First i have created the python file with Flask framework to display the output message which is "Hello Tamatem"
then i have tested the code using `python app.py` command to get the local url and test the code 
after that i started the containerzatiom process by creating a docker file and inside it i put all the required configuration to biuld an image for the application, after i finished the docker file i have applied the following command ` docker build -t  my-tamatem-app .` to build the image 
![image](https://github.com/HussamAlbadri/tamatem-task/assets/59113969/2cab49c6-3dd0-48a8-a39a-e8afcaf7303c)

after that i started to make the orchestration process for my docker images by defining the following deployment manifests:
### Deployment Manifest:
Create a deployment YAML file specifying:
Image name and tag (e.g., image: my-tamatem-app).
Replica count (e.g., replicas: 1).
Container definitions and port mappings.
### Service Manifest:
Create a service YAML file to expose the application:
Define a selector to match the deployment pods.
Specify the service port (e.g., port: 80).
Optionally, define a target port for the container port

then i built each of them by using the following command ` kubect apply -f <name>.yaml `

## The problems that i faced that when i get the local ip address to test the deployed app there was a kind of restrections from my pc firewall or traffic blocking so i could not detect the actual source of blocking 
