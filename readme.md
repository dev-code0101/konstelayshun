1. Application:  
   `<h1>Hello, World from Kubernetes!</h1>`
2. Local Kubernetes Setup:  
   Install Docker and Kind. Create a cluster:  
   `kind create cluster --name hello-world-cluster`  
   Verify with `kubectl get nodes`.

3. Docker Image:  
   Dockerfile:

```Dockerfile
FROM nginx:alpine
COPY app/index.html /usr/share/nginx/html/index.html
```

Build: `docker build -t hello-world-nginx .`  
Load to Kind: `kind load docker-image hello-world-nginx`.

4. Kubernetes Manifests:  
   Deployment YAML defines NGINX pod.  
   Apply: `kubectl apply -f k8s/`.

Access:  
Port forward to access the service from external ip: `kubectl port-forward svc/hello-world-service 8080:80`
Get NodePort and open in browser or curl `localhost:<port>`.
