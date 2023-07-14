# task_unbxd

I used Minikube instead of kind for this task.

1. I created the app.yaml to deploy a simple web app to serve a html page. It describes the deployment and service resources for a simple web application using an Nginx.
2. I then ran the following command to deploy the web application to the minikube cluster: "kubectl apply -f app.yaml"
3. I then ran "kubectl get pods" to check that our app pod is running or not.
4. When the pod was in running state, I ran "kubectl port-forward svc/web-app 8090:80" to access our app inside the cluster to 8090 port on localhost.
5. Finally I renamed the "localhost" to "adityajha.com" in /etc/hosts for our requirement.
![image](https://github.com/Muscleman1991/task_unbxd/assets/44231364/0bb10457-c658-4ada-8799-817391e520e7)
In the attached screen shot we can see that on hitting "http://adityajha.com:8090", We get the default Nginx page which is served by our app running in minikube.
