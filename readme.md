## Plan
- show dotnet aspire
- show aspirate 
- maybe show azure developer cli

## Steps
1. create a dotnet aspire app
2. run the app to show whats happenning
3. run aspire new to generate aspire app
    - aspire new
4. run (not needed)
    - dotnet run --publisher manifest --output-path manifest.json
5. use aspirate to generate k8s deployment
    - aspirate init
    - aspirate build
6. load images to minikube (if you are using not using docker-k8s)
    - minikube image ls 
    - minikube image load apiservice 
    - minikube image load webfrontends
    - minikube image ls 
7. generate and apply
    - aspirate generate
    - aspirate apply
8. kubectl
    - kubectl get deployments
    - kubectl get pods
    - kubectl get services
9. port forward
    - kubectl port-forward service/aspire-dashboard 18888:18888
    - kubectl port-forward service/webfrontend 8080:8080
10. destroy
    - aspirate destroy
11. remove images from minikube (if you are using not using docker-k8s)
    - minikube image ls 
    - minikube image rm apiservice 
    - minikube image rm webfrontends
    - minikube image ls 

## References
- https://learn.microsoft.com/en-us/dotnet/aspire/whats-new/dotnet-aspire-9.4 
- https://github.com/prom3theu5/aspirational-manifests
- https://medium.com/@josephsims1/aspire-aspi8-deploy-microservices-effortlessly-with-cli-no-docker-or-yaml-needed-f30b58443107 
- https://learn.microsoft.com/en-us/dotnet/core/docker/introduction 

