# Getting Started

In this section, you will have a look at the extension scenario that will be implemented and get access to the systems that will enable you for the next steps.

## Extension Scenario

JohnDoe Electronics is a growing e-commerce business selling electronic appliances to customers all around the world. They are using SAP Commerce Cloud and all of its features to offer customers the best experience, but as the business grows, they have some ideas on how to improve their service and overall satisfaction.

JohnDoe would like to implement the following improvements on their system:

1. Store all of their orders in a highly-available and peformant store like Redis - here we will learn how to deploy a Kyma Function and connect with CCv2 Events&APIs
2. Implement a customer-facing API that gives users information about their order - here we will learn how to use a Kyma Function as an API
3. Implement an internal API for the analytics team that retrieves common statistics - here we will learn how to deploy an ExpressJS application in Kyma as a microservice

In the upcoming exercises, you will be implementing these scenarios using the Kyma runtime for extending CCv2.

![scenario](./images/scenario.png)

## Prepare the environment

Before getting started with implementing the scenarios you will have to get access to the following systems:

1. A CCv2 tenant
2. A SAP BTP, Kyma runtime free trial

_❗ In order to facilitate the live session, the CCv2 tenants will be provided accordingly to users attending._

## Explore the systems

Finally, it's helpful to have a quick look and refresh the main dashboards you'll be using in the following exercises, namely:

1. CCv2 Backoffice
2. CCv2 Storefront
3. SAP BTP
4. Kyma Dashboard

## Summary

Congratulations, now you have understood the extension scenarios and provisioned the environment needed to implement everything.
Continue to - [Exercise 1 - Connecting CCv2 to Kyma](../ex1/README.md)
