# kubectl-tutorial
1. Create deployment node:![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/d6851870-2257-4a1b-b12b-a18302ce7845)

2. Get deployments: ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/9947622f-2575-45dd-b5f5-18166146d736)

3. Get pods: ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/1855fd30-eec0-4084-8c7b-e24e19efd6c7)
4. Get events: ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/221cf98c-e7b7-494d-bcbc-5fbc9e083272)
5. Config View: ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/8ac3e8d2-bb33-49c0-96c8-4956b8699917)
6. View application logs for a container in a pod:![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/aff3e57e-5bd3-4c55-bec6-c59959b60d1e)
7. I have some issues in running this first part of the tutorial, my minikube always runs to an error if I ran "minikube start". I tried to find the solution in stack overflow that states to use the command: "minikube start --no-vtx-check", and I did. If i ran it normally, I got this kind of error:
PS C:\Users\kenba> minikube start
W0517 15:48:14.014222   12472 main.go:291] Unable to resolve the current Docker CLI context "default": context "default": context not found: open C:\Users\kenba\.docker\contexts\meta\37a8eec1ce19687d132fe29051dca629d164e2c4958ba141d5f4133a33f0688f\meta.json: The system cannot find the path specified.
* minikube v1.33.1 on Microsoft Windows 11 Home Single Language 10.0.22621.3593 Build 22621.3593
* Automatically selected the virtualbox driver
* Downloading VM boot image ...
    > minikube-v1.33.1-amd64.iso....:  65 B / 65 B [---------] 100.00% ? p/s 0s
    > minikube-v1.33.1-amd64.iso:  314.16 MiB / 314.16 MiB  100.00% 2.29 MiB p/
* Starting "minikube" primary control-plane node in "minikube" cluster
* Downloading Kubernetes v1.30.0 preload ...
    > preloaded-images-k8s-v18-v1...:  342.90 MiB / 342.90 MiB  100.00% 2.12 Mi
* Creating virtualbox VM (CPUs=2, Memory=4000MB, Disk=20000MB) ...
! StartHost failed, but will try again: creating host: create: precreate: This computer doesn't have VT-X/AMD-v enabled. Enabling it in the BIOS is mandatory
* Creating virtualbox VM (CPUs=2, Memory=4000MB, Disk=20000MB) ...
* Failed to start virtualbox VM. Running "minikube delete" may fix it: creating host: create: precreate: This computer doesn't have VT-X/AMD-v enabled. Enabling it in the BIOS is mandatory

#  Create a Service:
1. Expose the Pod to the public internet:![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/170f4aa8-d4d0-4954-a606-e2ff1bdfc908)
2. View services I created: ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/5fa6d747-66d1-4847-a864-d903e57273b7)
3. ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/73020106-e4f4-483c-860a-b29311f9366d)
4. Application logs: ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/f5f715ed-6305-4de2-8b87-aac66bb93afe)

#    Monitor the Resource usage

1.![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/76054f89-12c0-4770-b4df-50c3ce00b529)
2. Enable metrics-server addons: ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/89671fdb-c6fe-41a8-a255-843accfab4f5)
3. Verify the Pod and Service related to the metrics server are created: ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/2443e08f-d9d1-4502-90b0-cb79e2b5cb90)
4. 


#    Reflection:
1. Before exposing the application as a Service, the logs only show initialization and internal activity within the pod. After exposing it as a Service, each time you access the application, new logs are generated for every request. These logs typically include details about incoming HTTP requests and responses. Opening the app multiple times increases the number of log entries. This increase demonstrates that the Service is routing traffic to the application, and the application is handling these requests.

2. The -n option in kubectl get specifies the namespace to query. Without any options, kubectl get defaults to the default namespace. Using -n kube-system queries the kube-system namespace, which contains Kubernetes system components. The output did not list the pods/services you explicitly created because they are in the default namespace, not in the kube-system namespace. Namespaces in Kubernetes isolate resources, so specifying the correct namespace is crucial to see the intended resources.


#    Rolling Update & Kubernetes Manifest File

#    Reflection:

1. o

2. 
3. ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/f66c7fb1-bfe3-4815-99c2-b585fdf63b23)
 ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/7cc90414-65ff-4884-9a14-f86b5b836e5f)
4. Using Kubernetes manifest files offers several benefits. They provide a clear, version-controlled, and reproducible way to define and manage application deployments, making the process more reliable and consistent. Manually deploying an app involves numerous steps that are prone to human error, whereas applying manifest files with kubectl apply -f simplifies and automates the process. This method ensures that deployments are documented and easily replicable across different environments. Overall, manifest files streamline deployment, improve collaboration, and enhance the maintainability of the application.







