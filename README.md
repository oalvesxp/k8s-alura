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

* kind
```
$ curl -Lo ./kind https://kind.sigs.k8s.io/dl/latest/kind-linux-amd64
$ chmod +x ./kind
$ sudo install kind /usr/local/bin/
```

* docker:
```
$ sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
</br>

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

3. kind:
```
$ kind --version
kind version 0.21.0-alpha+5549e9178ed153
```

4. docker:
```
$ docker -v
Docker version 24.0.7, build afdd53b
```
</br>

### Inicializando o minikube
---

```
$ kind create cluster
```
