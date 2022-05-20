create:
	kubectl create -f harbor-pv-local.yaml
	kubectl create -f harbor-pv-local-claim.yaml

delete:
	kubectl delete -f harbor-pv-local-claim.yaml
	kubectl delete -f harbor-pv-local.yaml
	
clean:
	rm -rf /opt/s4/harbor/registry
	mkdir -p /opt/s4/harbor/registry
	rm -rf /opt/s4/harbor/chartmuseum
	mkdir -p /opt/s4/harbor/chartmuseum
	rm -rf /opt/s4/harbor/jobservice
	mkdir -p /opt/s4/harbor/jobservice
	rm -rf /opt/s4/harbor/database
	mkdir -p /opt/s4/harbor/database
	rm -rf /opt/s4/harbor/redis
	mkdir -p /opt/s4/harbor/redis
	rm -rf /opt/s4/harbor/trivy
	mkdir -p /opt/s4/harbor/trivy

install:
	helm install -f values.yaml --namespace harbor harbor harbor/harbor

uninstall:
	helm -n harbor uninstall harbor

upgrade:
	helm upgrade -f values.yaml --namespace harbor harbor harbor/harbor