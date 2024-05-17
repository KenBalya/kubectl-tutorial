# kubectl-tutorial
1. Create deployment node:![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/d6851870-2257-4a1b-b12b-a18302ce7845)

2. Get deployments: ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/9947622f-2575-45dd-b5f5-18166146d736)

3. Get pods: ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/1855fd30-eec0-4084-8c7b-e24e19efd6c7)
4. Get events: ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/221cf98c-e7b7-494d-bcbc-5fbc9e083272)
5. Config View: ![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/8ac3e8d2-bb33-49c0-96c8-4956b8699917)
6. View application logs for a container in a pod:![image](https://github.com/KenBalya/kubectl-tutorial/assets/124903836/aff3e57e-5bd3-4c55-bec6-c59959b60d1e)
7. I have some issues in running this first part of the tutorial, my minikube always runs to an error if I ran "minikube run". I tried to find the solution in stack overflow that states to use the command: "minikube start --no-vtx-check", and I did. If i ran it normally, I got this kind of error:
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
4. 






