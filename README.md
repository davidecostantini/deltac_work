This repo contains the following files:

- build_and_deploy.yml => That's a Gitlab pipeline with 3 stages (test, build and deploy) which test the python code  using 'coverage' then, in case the tests succeed, proceed to build the container. At last, only on 'master' branch it simulate the deployment.

- k8s/certs_manager.yml => This is an helm file with that configure let's encrypt as certificate manager
- k8s/ingress.yml => That's the helm that configure the ingress controller using TLS
- k8s/mongodb-deployment.yml => Deployment file that configure MongoDB, considering this is a staful service it configure a persisten volume
- k8s/myapp-deployment.yml => Deployment of the service called 'myapp' using 'hello-app' container from Google to simulate a service
- k8s/myapp-svc.yml => Here we configure 'myapp' service


These files are just to show how the config will look like and won't be fully working as we don't own the DNS domain and we're not in a position to create a certificate with that hostname.