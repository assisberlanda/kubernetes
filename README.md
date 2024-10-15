![](https://img.shields.io/badge/Start-Minikube-orange)

	minikube start
#### Status
	minikube status
#### Entrar no Pod
	minikube ssh
#### [Instalar kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/)
    curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/amd64/kubectl"
#### ![](https://img.shields.io/badge/Iniciar-Kubernetes-brightgreen)
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
![](https://img.shields.io/badge/Verificar-Serviço-red)
	
 	kubectl get service
Para o Minikube para pegar a URL digita o comando abaixo
Na vida real gera ip automático

	minikube service --url app-html



![](https://shields.io/community#assis)
![rating](https://img.shields.io/opencollective/backers/shields)
![rating](https://shields.io/community#assis)
![rating](https://img.shields.io/opencollective/sponsors/shields)
![rating](https://github.com/badges/shields/pulse)
![rating](https://img.shields.io/github/commit-activity/m/badges/shields)
![rating](https://github.com/badges/shields/discussions")
![rating](https://img.shields.io/github/discussions/badges/shields)
![rating](https://github.com/badges/shields/actions/workflows/daily-tests.yml)
![rating](https://img.shields.io/github/actions/workflow/status/badges/shields/daily-tests.yml?label=daily%20tests)
![rating](https://coveralls.io/github/badges/shields)
![rating](https://img.shields.io/coveralls/github/badges/shields)
![rating](https://discord.gg/HjJCwm5)
![rating](https://img.shields.io/discord/308323056592486420?logo=discord&logoColor=white)
![rating](https://img.shields.io/badge/any_text-you_like-blue)
   
