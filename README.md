# setup recorrente
Abrir Docker

wsl
cd ~

minikube start
minikube stop
minikube delete

wsl --shutdown (no powershell)

# kubectl+installation
Install kubectl

1. Open download folder
$ cd Download

2. Download kubectl
$ curl -LO https://dl.k8s.io/release/v1.24.2/bin/linux/amd64/kubectl

3. Install kubectl
$ sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

4. Check installation
$ kubectl version --client --output=yaml   

# minikube+install

minikube install (Local Kubernetes cluster)

1. Open download folder
$ cd Download

2. Download minikube
$ curl -Lo minikube https://storage.googleapis.com/minikube/releases/v1.26.0/minikube-linux-amd64

3. Set permission
$ chmod +x minikube

4.Install minikube
$ sudo install minikube /usr/local/bin/

5. Configure user group
$ sudo usermod -aG docker $USER

6. Reboot Linux
$ sudo reboot

7. Initialization
$ minikube delete
$ minikube start
