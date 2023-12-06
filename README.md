## k8s-alura
Curso de Kubernetes na Alura.

* Livro Gratuito para estudo de Kubernetes: <a href="https://livro.descomplicandokubernetes.com.br/pt/">LINUXtips</a>


### Dependências
---

* kubectl
```
$ sudo apt update
$ sudo apt install -y ca-certificates curl
$ sudo apt install -y apt-transport-https
$ curl -fsSL https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-archive-keyring.gpg
$ echo "deb [signed-by=/etc/apt/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list
$ sudo apt update
$ sudo apt install kubectl -y
```

* minikube
```
$ curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-arm64
$ chmod +x ./minikube
$ sudo install minikube-linux-arm64 /usr/local/bin/
```
</br>

* Virtualizador: </br>
*Estou procurando uma solução para o virtualizador.*</br>
*O virtualbox apresenta problemas com a configuração de network:*
```
Error setting up host only network on machine start: /usr/bin/VBoxManage hostonlyif ipconfig vboxnet2 --ip 192.168.99.1 --netmask 255.255.255.0 failed:
```


### Versões
---

1. Sistema Operacional:
```
$ hostnamectl | grep -i "operating system"
Operating System: Debian GNU/Linux 12 (bookworm)
```

2. kubectl:
```
$ kubectl version --client
Client Version: v1.28.4
Kustomize Version: v5.0.4-0.20230601165947-6ce0bf390ce3
```

3. minikube:
```
$ minikube version
minikube version: v1.12.1
commit: 5664228288552de9f3a446ea4f51c6f29bbdd0e0-dirty
```

4. virtualbox:
```
$ vboxmanage -v | cut -dr -f1
7.0.12
```
</br>

### Inicializando o minikube
---

```
$ minikube start --vm-driver=virtualbox
```
