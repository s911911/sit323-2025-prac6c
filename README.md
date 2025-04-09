SIT323-6.2C: Interacting with Kubernetes Cluster

1.This task builds upon the previous SIT323-6.1P work. The objective is to further interact with the Kubernetes cluster and verify the deployment using `kubectl`, and expose the service to the local machine via port forwarding.

2. Apply Kubernetes Configurations
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

3. Verify the Application is Running
kubectl get pods
kubectl get services
You should see your pod running and a service of type ClusterIP or NodePort (based on your config).

4. Use Port Forwarding to Access the Application
Identify the pod name first:
kubectl get pods
Then run:
kubectl port-forward pod/container-7475d54758-szckg 2080:2000
This command maps the local machine's port 2080 to the pod's internal container port 2000.

5. Access the Application in Browser
Open a browser and go to:
http://localhost:2080

