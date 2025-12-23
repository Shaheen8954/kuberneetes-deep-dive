configmap is a k8s object that we use for k8s configuration and it is a key value pair.

We can use configmap in two ways:
1. as environment variables for a container
2. as files in read-only volume, for the application to read.
3. Inside a  container command and args, 
4. Write code to run inside the pod that use the kubernetes API to read the ConfigMap.

- When we change configmap we need to restart application to pick up the new configmap.

- If we add -
immutable: true
then we can not update configmap. Only can delete and create new configmap.

