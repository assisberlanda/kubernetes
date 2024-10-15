## ✅ [Criar um Cluster](https://kubernetes.io/pt-br/docs/tutorials/kubernetes-basics/_print/)
## 🆑 [Principais Comandos](https://ebasso.net/wiki/index.php?title=Kubernetes:_Principais_Comandos)

![](https://img.shields.io/badge/Start-Minikube-orange)

	minikube start
#### Status
	minikube status
#### Entrar no Pod
	minikube ssh
#### [Instalar kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/)
    curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/amd64/kubectl"
#### Iniciar um Kubernetes
	kubectl apply -f simple-pod.yml
#### Serviços
	kubectl get services
#### Visualizar Pods
	kubectl get pods
	kubectl get pods -o wide
#### Visualizar deployments
	kubectl get deployment
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
#### Expose Deployment para Load Balancer
	kubectl expose deployment app-html-deployment --type=LoadBalancer --name=app-html --port=80
![](https://img.shields.io/badge/Verificar-Serviço-red)
	
 	kubectl get service
Para o Minikube pegar a URL digita o comando abaixo
Na vida real gera ip externo automático

	minikube service --url app-html
 #### Para excluir o Load Balancer e Criar um em YAML
 	kubectl get service
  	kubectl delete service app-html
### Arquivo YAML
| Pod | apiVersion: v1 |
|-|-|
| Deployment | apiVersion: app/v1 |
| Service    | apiVersion: v1     |
 Crie um app-html-lb.yml
 ## ❗️ Arquivo YAML para Load Balancer
	apiVersion: v1
	kind: Service
	metadata: 
  	  name: app-html-lb
	spec:
  	  selector:
    	    app: app-html
  	  ports:
    	    - port: 80
      	      targetPort: 80
 	  type: LoadBalancer
