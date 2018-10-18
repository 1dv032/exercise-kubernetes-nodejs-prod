# exercise-kubernetes-nodejs-prod
In this exercise you should "convert" a docker-compose environment to kubernetes.

## First navigate to your exercise repository
```bash
git remote add kubernetes-nodejs-prod https://github.com/1dv032/exercise-kubernetes-nodejs-prod/
git subtree add --prefix=kubernetes-nodejs-prod --squash kubernetes-nodejs-prod master
cd kubernetes-nodejs-prod
```
You should now have a folder called kubernetes-nodejs-prod in your exercise repo.

## The assignment
You will continue on from the last exercise, you have previously created a production environment for a simple web application using docker-compose.
You should now convert that into a Kuvernetes environment and the requirements are similar to the once in the previous exercise.

### Requirement

* The application should be publicly accessible from the Internet
* It should use a Load balancer, created by Kubernetes not an image, in front that directs traffic to the reverse proxy
* You should have at least 2 replicas of the application running at all times
* The application docker image should be hosted on your own private docker registry
* The reverse proxy should use a official nginx image
  * nginx configuration should be loaded via kubernetes configuration maps
  * certificate should not be baked in the image, it should use kubernetes secrets

## Resources
* Creating self-signed certificate
* (https://github.com/kubernetes/examples/tree/master/staging/https-nginx)