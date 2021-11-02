# ISP261 - Extend SAP Commerce Cloud Through Cloud Native Functions and Services

## Description

This repository contains the material for the SAP TechEd 2021 session called ISP261 - Extend SAP Commerce Cloud Through Cloud Native Functions and Services.

## Overview

In this session we will walk you through an overview of how to extend SAP Commerce Cloud using SAP Cloud Platform, Kyma runtime - a Kubernetes-based open-source platform. You will learn how to use microservices combined with serverless functions and events to create a modern extension scenario for Commerce that will fit your business needs. Furthermore, understand why using this platform is the recommended approach to build extension scenarios and drive innovation for your Intelligent Enterprise.

## Requirements

❗ _It is very important that the two steps below are completed before the day of the session, they will enable you to follow the rest of the exercises._

- Get a free trial account on SAP BTP; see this [tutorial](https://developers.sap.com/tutorials/hcp-create-trial-account.html).
- Enable Kyma runtime on your newly created SAP BTP account; see this [tutorial](https://developers.sap.com/tutorials/cp-kyma-getting-started.html).

😊 _Furthermore, while not obligatory, for this session you also need a local development system. You will have a better experience if you have the applications listed below installed._

- VSCode - download [here](https://code.visualstudio.com/)
- Node.js - download [here](https://nodejs.org/en/download/)
- Docker and a Docker hub account ( Docker ID ) - download [here](https://www.docker.com/products/docker-desktop)

## Exercises

- [Getting Started](exercises/ex0/)
- [Exercise 1 - Connecting CCv2 to Kyma](exercises/ex1/)

  - [Exercise 1.1 Create a System](exercises/ex1#exercise-11-create-a-system)
  - [Exercise 1.2 Create a Formation](exercises/ex1#exercise-12-create-a-formation)
  - [Exercise 1.3 Pair an application](exercises/ex1#exercise-13-pair-an-application)
  - [Exercise 1.4 Check connection](exercises/ex1#exercise-14-check-connection)

- [Exercise 2 - Exploring Exposed Events and APIs](exercises/ex2/)

  - [Exercise 2.1 Bind CCv2 to a namespace](exercises/ex2#exercise-21-bind-ccv2-to-a-namespace)
  - [Exercise 2.2 Create the Events service instance](exercises/ex2#exercise-22-create-the-events-service-instance)
  - [Exercise 2.3 Create the API service instance](exercises/ex2#exercise-23-create-the-api-service-instance)
  - [Exercise 2.4 View the Service Instances](exercises/ex2#exercise-24-view-the-service-instances)

- [Exercise 3 - Implementing Extension Scenario 1: Function](exercises/ex3/)

  - [Exercise 3.1 Deploy the Redis cache](exercises/ex3#exercise-31-deploy-the-redis-cache)
  - [Exercise 3.2 Deploy your first Function](exercises/ex3#exercise-32-deploy-your-first-function)
  - [Exercise 3.3 Subscribe the Function to Events and APIs](exercises/ex3#exercise-33-subscribe-the-function-to-events-and-apis)
  - [Exercise 3.4 Test out the connection](exercises/ex3#exercise-34-test-out-the-connection)
  - [Exercise 3.5 Configure your Function resources](exercises/ex3#exercise-35-configure-your-function-resources)
  - [Exercise 3.6 Implement the rest of your Function](exercises/ex3#exercise-36-implement-the-rest-of-your-function)
  - [Exercise 3.7 Implement a reading API](exercises/ex3#exercise-37-implement-a-reading-api)

- [Exercise 4 - Implementing Extension Scenario 2: Microservice](exercises/ex4/)

  - [Exercise 4.1 Bootstrap the project](exercises/ex4#exercise-41-bootstrap-the-project)
  - [Exercise 4.2 Dockerize the microservice](exercises/ex4#exercise-42-dockerize-the-microservice)
  - [Exercise 4.3 Time for Kubernetes](exercises/ex4#exercise-43-time-for-kubernetes)
  - [Exercise 4.4 Deploy resources into Kyma](exercises/ex4#exercise-44-deploy-resources-into-kyma)
  - [Exercise 4.5 Implement the rest of the microservice](exercises/ex4#exercise-45-implement-the-rest-of-the-microservice)
  - [Exercise 4.6 Redeploy and test out our endpoints](exercises/ex4#exercise-46-redeploy-and-test-our-endpoints)

- [(Bonus) Exercise 5 - Monitoring with Kyma built-in tools](exercises/ex5/)
  - [Exercise 5.1 - Open the monitoring tools](exercises/ex5#exercise-51-open-the-monitoring-tools)
  - [Exercise 5.2 - Watch logs in Grafana and Loki](exercises/ex5#exercise-52-watch-logs-in-grafana-and-loki)
  - [Exercise 5.3 - Visualize metrics in Grafana and Prometheus](exercises/ex5#exercise-53-visualize-metrics-in-grafana-and-prometheus)

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## Contributing

The content of this repository is targeting the session ISP261 - Extend SAP Commerce Cloud Through Cloud Native Functions and Services at SAP TechEd 2021. Only sesson speakers will make contributions to this repository. If you wanna enhance the content of this repository feel free to fork it.

## Disclaimer

In order to facilitate the session and complete the exercises in this workshop, a CCv2 tenant is paramount and will be provided by the speakers to all listeners during the session. These CCv2 tenants will be available only for a short duration following the session, and for this reason, the session will not be recorded and the workshop can only be attended live.

## License

Copyright (c) 2021 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
