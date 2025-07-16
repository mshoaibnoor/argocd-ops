//ingress installation and configuration
https://github.com/marcel-dempers/docker-development-youtube-series/blob/master/kubernetes/ingress/controller/nginx/README.md


helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm search repo ingress-nginx --versions

helm template ingress-nginx ingress-nginx \
--repo https://kubernetes.github.io/ingress-nginx \
--version ${CHART_VERSION} \
--namespace ingress-nginx \
> nginx-ingress.${APP_VERSION}.yaml