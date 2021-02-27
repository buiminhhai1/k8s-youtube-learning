## Add domain for etc/host (DNS your machine with command bellow)
* ```echo "$(minikube ip) dashboard-mongo-express.com" | sudo tee -a /etc/hosts``` or using 