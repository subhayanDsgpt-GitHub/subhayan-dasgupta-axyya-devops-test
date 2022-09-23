# subhayan-dasgupta-axyya-devops-test
AXYYA DIGITAL - DevOps Engineer Role - L1B - Assessment - REVISED

## Packaging the sample_app into a container

Following steps are followed during containerization:
- Docker stack is used to package the app.js.
- package.json file has been created to describe the app and its dependencies.
- "npm install" command has been ran to generate the package-lock.json file which will be copied to your Docker image.
- server.js file has been created to define the sample_app using the Express.js framework.
- The Dockerfile and .dockerignore files are created respectively to define the parameters of containerization.
- To build the container image of the sample_app, following commands are run on the terminal
    - docker build . -t <your username>/sample_app
    - docker images
    - docker run -p 49160:8080 -d <your username>/sample_app
    - docker ps
    - curl -i localhost:49160


## Deploying the prebuilt image into Kubernetes

Following steps are followed during deploying into Kubernetes:
- To store the prebuild image of the sample_app, DockerHub [subhayandsgpt/sample_app](https://hub.docker.com/repository/docker/subhayandsgpt/sample_app) has been used.
- Kubernetes YAML file has been created to describe sample_app.
- To deploy the image of the sample_app onto Kubernetes, following commands are run on the terminal
    - kubectl apply -f <file_name>.yaml
    - kubectl get deployments
    - kubectl get services


## 