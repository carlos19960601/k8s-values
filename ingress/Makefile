install:
	helm install -f values.yaml ingress-nginx ingress-nginx/ingress-nginx -n ingress-nginx

uninstall:
	helm -n ingress-nginx uninstall ingress-nginx

upgrade:
	helm upgrade -f values.yaml --namespace ingress-nginx ingress-nginx ingress-nginx/ingress-nginx