# Deployment of Hotel service on kubernetes using Minikube 

1. Prepare Docker Images: Build Docker images for your hotel service and MySQL database. Ensure that you have Dockerfiles for both services and that the images are properly configured.
2. Start Minikube: Start Minikube by running minikube start. This will create a local Kubernetes cluster.
3. Set Up MySQL Deployment: Create a Kubernetes Deployment for MySQL. You'll need to define a Deployment YAML file with specifications for the MySQL container, including environment variables for database credentials, volume mounts for persistent storage, etc.
4. Set Up MySQL Service: Create a Kubernetes Service for MySQL to allow other components to communicate with the MySQL database. You can use a ClusterIP type service for internal communication within the cluster.
5. Set Up Hotel Service Deployment: Create a Kubernetes Deployment for your hotel service. Define a Deployment YAML file with specifications for the hotel service container, including environment variables for connecting to the MySQL database, ports, etc.
6. Set Up Hotel Service Service: Create a Kubernetes Service for your hotel service. You can use a NodePort type service to expose your hotel service externally (optional).
7. Apply Configurations: Apply the MySQL and hotel service Deployment and Service configurations using kubectl apply.
8. Verify Deployments: Use kubectl get pods, kubectl get services, etc., to verify that your MySQL and hotel service pods and services are running and accessible.
9. Test Connectivity: Test connectivity between your hotel service and MySQL database to ensure they can communicate properly.
10. Test Hotel Service: Test your hotel service to ensure it's functioning correctly. You can send requests to its endpoints and verify that it interacts with the MySQL database as expected.
11. Optional: Expose Hotel Service: If you didn't already expose your hotel service in step 6, you can create an additional service of type NodePort or LoadBalancer to expose it externally.
12. Cleanup: Once you're done testing, you can delete the resources by running kubectl delete deployment <deployment_name> and kubectl delete service <service_name> for both the hotel service and MySQL, and then stop Minikube with minikube stop.