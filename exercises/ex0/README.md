# Getting Started

In this section, you will have a look at the extension scenarios that you'll be implementing in the coming hours and get access to the systems that will enable you throughout the workshop.

## Extension Scenario

JohnDoe Electronics is a growing e-commerce business selling electronic appliances to customers all around the world. They are using SAP Commerce Cloud and all of its features to offer customers the best experience, but as the business grows, they have some ideas on how to improve their service and overall satisfaction.

JohnDoe would like to implement the following improvements on their system:

1. Store all of their orders in a highly-available and peformant store like Redis - you will learn how to deploy a Function and connect Kyma with CCv2 Events and APIs.
2. Implement a customer-facing API that gives users information about their order - you will learn how to use a Kyma Function as an API.
3. Implement an internal API for the analytics team that retrieves common statistics - you will learn how to build and deploy an ExpressJS application in Kyma as a microservice.

In the upcoming exercises, you will be implementing these scenarios using the Kyma runtime for extending CCv2.

![scenario](./images/scenario.png)

## Prepare the environment

Before getting started with the exercises you have to get access to the following systems:

1. SAP BTP, Kyma runtime free trial - **As part of the prerequisites, it is expected that every listener already has access to a free trial SAP BTP account and enabled the Kyma runtime.**
2. CCv2 tenant - **A list of provisioned tenants is shown below and will be distributed to the listeners based on attendance during the live session.**

| Tenant Name |                                  Storefront URL                                  |                                                                                 Backoffice URL |
| :---------- | :------------------------------------------------------------------------------: | ---------------------------------------------------------------------------------------------: |
| Tenant 1    | https://jsapps.cp96avkh5f-techedses1-d2-public.model-t.cc.commerce.ondemand.com/ | https://backoffice.cp96avkh5f-techedses1-d2-public.model-t.cc.commerce.ondemand.com/backoffice |
| Tenant 2    | https://jsapps.cp96avkh5f-techedses1-d3-public.model-t.cc.commerce.ondemand.com/ | https://backoffice.cp96avkh5f-techedses1-d3-public.model-t.cc.commerce.ondemand.com/backoffice |
| Tenant 3    | https://jsapps.cp96avkh5f-techedses1-d4-public.model-t.cc.commerce.ondemand.com/ | https://backoffice.cp96avkh5f-techedses1-d4-public.model-t.cc.commerce.ondemand.com/backoffice |
| Tenant 4    | https://jsapps.cp96avkh5f-techedses1-d5-public.model-t.cc.commerce.ondemand.com/ | https://backoffice.cp96avkh5f-techedses1-d5-public.model-t.cc.commerce.ondemand.com/backoffice |
| Tenant 5    | https://jsapps.cp96avkh5f-techedses1-d6-public.model-t.cc.commerce.ondemand.com/ | https://backoffice.cp96avkh5f-techedses1-d6-public.model-t.cc.commerce.ondemand.com/backoffice |
| Tenant 6    | https://jsapps.cp96avkh5f-techedses1-d7-public.model-t.cc.commerce.ondemand.com/ | https://backoffice.cp96avkh5f-techedses1-d7-public.model-t.cc.commerce.ondemand.com/backoffice |
| Tenant 7    | https://jsapps.cp96avkh5f-techedses1-d8-public.model-t.cc.commerce.ondemand.com/ | https://backoffice.cp96avkh5f-techedses1-d8-public.model-t.cc.commerce.ondemand.com/backoffice |
| Tenant 8    | https://jsapps.cp96avkh5f-techedses1-d9-public.model-t.cc.commerce.ondemand.com/ | https://backoffice.cp96avkh5f-techedses1-d9-public.model-t.cc.commerce.ondemand.com/backoffice |

## Explore the systems

Finally, it's helpful to have a first peek at the main dashboards you'll be using in the following exercises and keep the tabs open on the side:

1. CCv2 Storefront
2. CCv2 Backoffice
3. SAP BTP
4. Kyma Dashboard

## Summary

Congratulations, you have now understood the extension scenarios that will be implemented and got access to all the needed environments.
Continue to - [Exercise 1 - Connecting CCv2 to Kyma](../ex1/README.md)
