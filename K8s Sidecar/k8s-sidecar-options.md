Apply the configuration with this command:

`kubectl apply -f nginx-jenkins-sidecar.yaml`

Forward port 80 from the pod so that it can be accessed from your machine:

`kubectl port-forward jenkins 9000:80`

Access the Application:

`Enter http://<IP>:9000/jenkins into your browser.`

Check the NGINX Logs:

`kubectl logs pods/jenkins -c jenkins`

Delete the Pod and ConfigMap that was created by running this command:

`kubectl delete -f pods/jenkins`