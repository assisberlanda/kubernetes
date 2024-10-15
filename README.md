#### Start Minikube
	minikube start
#### Status
	minikube status
#### Entrar no Pod
	minikube ssh
#### [Instalar kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/)
    curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/amd64/kubectl"
#### Iniciar Pod kubernetes
	kubectl apply -f simple-pod.yml
#### Serviços
	kubectl get services
#### Visualizar Pods
	kubectl get pods
	kubectl get pods -o wide
#### Visualizar Nós
	kubectl get nodes
#### Descrição Nodes
	kubectl describe nodes minikube
#### Deletar Pod
	kubectl delete pod app-html
#### Site [Kubectl deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)
#### Visualizar Kubernetes Deployment
	kubectl describe deployment app-html-deployment
#### Escalar por CLI Pods
	kubectl scale deployment app-html-deployment --replicas=10
#### Explore Deployment para Load Balancer
	kubectl expose deployment app-html-deployment --type=LoadBalancer --name=app-html --port=8
#### Verifica Serviço
	kubectl get service
Para o Minikube para pegar a URL digita o comando abaixo
Na vida real gera ip automático

	minikube service --url app-html



