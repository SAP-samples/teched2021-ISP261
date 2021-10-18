# Getting Started

In this section, you will have a look at the extension scenario that will be implemented and get access to the systems that will enable you for the next steps.

## Extension Scenario

JohnDoe Electronics is a growing e-commerce business selling electronic appliances to customers all around the world. They are using SAP Commerce Cloud and all of it's features to offer customers the best experience, but as the business grows, they have some ideas
on how to improve their service and overall satisfaction.

JohnDoe would like to implement two improvements on their system:

1. Store all of their orders in a highly-available and peformant cache like Redis for future real-time analysis like anti-spam etc. For implementing this simple extension, Kyma functions are a great fit.
2. Every time a customer completes an order that is greater than $200, JonDoe wants to send a personalized thank-you email to the customer and ask on their satisfaction levels. Given that this extension is a bit more sophisticated, you will be using a microservice approach.

In the upcoming exercises, you will be implementing these scenarios using the Kyma runtime for extending CCv2.

![scenario](./images/scenario.png)

## Prepare the environment

Before getting started with implementing the scenarios you will have to get access to the following systems:

1. A CCv2 tenant
2. A SAP BTP, Kyma runtime free trial

_In order to facilitate the live session, the CCv2 tenants will be provided accordingly to users attending._

## Explore the systems

Finally, it's helpful to have a quick look and refresh the main dashboards you'll be using in the following exercises, namely:

1. CCv2 Backoffice
2. CCv2 Storefront
3. SAP BTP
4. Kyma Dashboard

## Summary

Congratulations, now you have understood the extension scenarios and provisioned the environment needed to implement everything.
Continue to - [Exercise 1 - Exercise 1 Description](../ex1/README.md)
