https://learning.kasten.io/kubernetes/labs/first-kubernetes-cluster/lessons/lab-1/#lab

git clone https://github.com/microservices-demo/microservices-demo.git

cd microservices-demo/deploy/kubernetes

kubectl apply -f complete-demo.yaml

deployment "carts-db" created
service "carts-db" created
deployment "carts" created
service "carts" created
deployment "catalogue-db" created
service "catalogue-db" created
deployment "catalogue" created
service "catalogue" created
deployment "front-end" created
service "front-end" created
deployment "orders-db" created
service "orders-db" created
deployment "orders" created
service "orders" created
deployment "payment" created
service "payment" created
deployment "queue-Control Plane" createdwatch kubectl get pods --namespace sock-shop
service "queue-Control Plane" created
deployment "rabbitmq" created
service "rabbitmq" created
deployment "shipping" created
service "shipping" created
deployment "user-db" created
service "user-db" created
deployment "user" created
service "user" created


watch kubectl get pods --namespace sock-shop

NAMESPACE     NAME                              READY     STATUS    RESTARTS   AGE
sock-shop     carts-74f4558cb8-h9924            1/1       Running   0          11m
sock-shop     carts-db-7fcddfbc79-v64fw         1/1       Running   0          11m
sock-shop     catalogue-676d4b9f7c-55n4g        1/1       Running   0          11m
sock-shop     catalogue-db-5c67cdc8cd-hvk96     1/1       Running   0          11m
sock-shop     front-end-977bfd86-hq9x9          1/1       Running   0          11m
sock-shop     orders-787bf5b89f-xfdl6           1/1       Running   0          11m
sock-shop     orders-db-775655b675-gv456        1/1       Running   0          11m
sock-shop     payment-75f75b467f-4zzqs          1/1       Running   0          11m
sock-shop     queue-Control Plane-5c86964795-t8sjg     1/1       Running   0          11m
sock-shop     rabbitmq-96d887875-lf46w          1/1       Running   0          11m
sock-shop     shipping-5bd69fb4cc-vprmp         1/1       Running   0          11m
sock-shop     user-5bd9b9c468-4rms8             1/1       Running   0          11m
sock-shop     user-db-5f9d89bbbb-r69pd          1/1       Running   0          11m


[![Build Status](https://travis-ci.org/microservices-demo/microservices-demo.svg?branch=master)](https://travis-ci.org/microservices-demo/microservices-demo)

# Sock Shop : A Microservice Demo Application

The application is the user-facing part of an online shop that sells socks. It is intended to aid the demonstration and testing of microservice and cloud native technologies.

It is built using [Spring Boot](http://projects.spring.io/spring-boot/), [Go kit](http://gokit.io) and [Node.js](https://nodejs.org/) and is packaged in Docker containers.

You can read more about the [application design](./internal-docs/design.md).

## Deployment Platforms

The [deploy folder](./deploy/) contains scripts and instructions to provision the application onto your favourite platform. 

Please let us know if there is a platform that you would like to see supported.

## Bugs, Feature Requests and Contributing

We'd love to see community contributions. We like to keep it simple and use Github issues to track bugs and feature requests and pull requests to manage contributions. See the [contribution information](.github/CONTRIBUTING.md) for more information.

## Screenshot

![Sock Shop frontend](https://github.com/microservices-demo/microservices-demo.github.io/raw/master/assets/sockshop-frontend.png)

## Visualizing the application

Use [Weave Scope](http://weave.works/products/weave-scope/) or [Weave Cloud](http://cloud.weave.works/) to visualize the application once it's running in the selected [target platform](./deploy/).

![Sock Shop in Weave Scope](https://github.com/microservices-demo/microservices-demo.github.io/raw/master/assets/sockshop-scope.png)

## 
