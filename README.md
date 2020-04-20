# Udagram Application
Udagram is a microservice based application, it allows users to register, login, and post photos on the web frontend application.

Application dependencies:
Nodejs, Docker, Kubernestes, AWS, TravisCI

Steps to run the application:
1. Clone the respository : git clone  https://github.com/ArjunSingh007/udagram-refactor.git 
2. Change the folder : cd udacity-c3-deployment/docker
3. Build all the images: docker-compose -f docker-compose-build.yaml build --parallel
4. Run the container: docker-compose up
5. Push to code to github for build using TravisCI

To run the container in Kubernetes as a pod:
1. Change the folder : cd udacity-c3-deployment/k8s.
2. Modify the aws-secret.yaml, env-configmap.yaml and env-secret.yaml.
3. Create services (deployments, service, secret, pods) using all the yaml file present in the folder: kubectl apply -f file-name.yaml
4. Test the application: search http://localhost:8100, register, post photos.
