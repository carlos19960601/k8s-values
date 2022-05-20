create:
	kubectl create -f gitea-pv-local.yaml
	kubectl create -f gitea-pv-local-claim.yaml

delete:
	kubectl delete -f gitea-pv-local-claim.yaml
	kubectl delete -f gitea-pv-local.yaml
	
clean:
	rm -rf /opt/s4/gitea
	mkdir -p /opt/s4/gitea

install:
	helm install -f values.yaml --namespace gitea gitea gitea-charts/gitea

uninstall:
	helm -n gitea uninstall gitea

upgrade:
	helm upgrade -f values.yaml --namespace gitea gitea gitea-charts/gitea