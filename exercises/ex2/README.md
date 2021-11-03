# Exercise 2 - Explore exposed APIs and Events

In this second exercise, you will explore the events and APIs exposed from the CCv2 tenant and follow the necessary steps to start using them.

## Exercise 2.1 Bind CCv2 to a namespace

The very first thing you need to do is bind the CCv2 application to the Kyma namespace that will contain all your extensions. This will allow the APIs and Events of CCv2 to be used within the namespace.

1. In the Kyma home workspace, click on the `Integration > Applications/Systems` menu.
2. Choose the `mp-your-app-name` application by clicking on the name value shown in the list. It's status should appear as `NOT_SERVING`.

![Select Application](./images/1.png)

3. Click on the option `Create Binding`.

![Create Binding](./images/2.png)

4. In the Namespace select list choose the option `default` and then click on `Create`.

![Create Binding](./images/3.png)

1. You should now see the list of Events/APIs exposed from CCv2 that you can start using.

![Events and Services](./images/4.png)

## Exercise 2.2 Create the Events service instance

For the extension scenarios discussed earlier, you will need to keep track of all orders coming from CCv2. This can be done via a `Subscription` to the `orderCreated` event. But before you create the event subscription, you need to create a service instance from the exposed Events.

1. In the Kyma home workspace, choose `Namespace` and select the `default` namespace.

![Select Namespace](./images/5.png)

2. Within the default namespace, choose `Service Management > Catalog`.

![Select catalog](./images/6.png)

3. Choose the tile first Tile that indicates the CCv2 application. There you can view the Service Class Plans of the application.

![Service tile](./images/7.png)

4. Choose the Service Class Plan for `CC Events v1`. Click on `Add` and then `Create` to create a Service Instance.

![Events](./images/8.png)

You will then be landed in the newly created service instance, now ready to use.

## Exercise 2.3 Create the API service instance

For the extension scenarios you also need a CCv2 API that allows you to get additional order details following the event. In this step you will subscribe to the `OCC API` services exposed from CCv2 that gives you access to those endpoints.

1. Following the same steps as the exercise above, choose `Service Management > Catalog > CC OCC Commerce Webservices v2`.

![API service tile](./images/10.png)

2. Choose `Add` and then `Create` to create a Service Instance.

![Create API service](./images/9.png)

## Exercise 2.4 View the Service Instances

In this step you will view the Events and the OCC Webservices service instances created in the previous two steps.

In the default namespace, choose `Service Management > Instances`. This view will list the service instances existing in the namespace.

![View instances](./images/11.png)

If everything is sucessful, you should see the status of the two service instnaces as `Running`.

## Summary

Great job! You've now created service instances for Events and OCC APIs and you are ready to start implementing the extension scenarios.

Continue to - [Exercise 3 - Implementing Extension Scenario 1: Functions](../ex3/README.md)
