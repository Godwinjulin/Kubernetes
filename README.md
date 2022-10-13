
# Run the app in Kubernetes
The folder k8s-specifications contains the yaml specifications of the Voting App's services.

First create the vote namespace

$ kubectl create namespace vote

Run the following command to create the deployments and services objects:

$ kubectl create -f k8s-specifications/

deployment "db" created

service "db" created

deployment "redis" created

service "redis" created

deployment "result" created

service "result" created

deployment "vote" created

service "vote" created

deployment "worker" created

The vote interface is then available on port 31000 on each host of the cluster, the result one is available on port 31001.

Architecture

![Screenshot 2022-10-13 at 17 12 37](https://user-images.githubusercontent.com/96737660/195660247-90b45f23-947b-4e80-9582-06da84223bb0.png)

