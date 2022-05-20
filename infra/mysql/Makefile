create:
	kubectl create -f mysql-pv-local.yaml
	kubectl create -f mysql-pv-local-claim.yaml

delete:
	kubectl delete -f mysql-pv-local-claim.yaml
	kubectl delete -f mysql-pv-local.yaml
	
clean:
	rm -rf /opt/s4/mysql/primary
	mkdir /opt/s4/mysql/primary

install:
	helm install -f values.yaml --namespace infra  dm-mysql bitnami/mysql 

uninstall:
	helm uninstall dm-mysql

upgrade:
	helm upgrade -f values.yaml --namespace infra  dm-mysql bitnami/mysql 