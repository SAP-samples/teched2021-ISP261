# Exercise 1 - Connect Kyma To CCv2

In this exercise you will create a connection between CCv2 and SAP BTP, Kyma runtime. With this connection in place you can start subscribing to events and consuming APIs coming from CCv2.

## Exercise 1.1 Create a System

As a first step, you will create a System at the Global account level of your SAP BTP account which will be used to pair the CCv2 application to the Kyma runtime.

1. Open your Global SAP BTP account and choose the `System Landscape > Systems` menu options.

![Register System](./images/1-register-system.png)

2. Click the `Register System` option, provide the name, set the type to `SAP Commerce Cloud` and then choose `Register`.

![System Details](./images/2-give-system-details.png)

3. Copy the `Token` value, store it somewhere safe and close the window. This value will expire in five minutes and will be needed in a subsequent step.

![Token generated](./images/3-token-generated.png)

**Note**: If the token expires before use, you can obtain a new one by choosing the `Display Token` option shown next to the entry in the `Systems` list.

## Exercise 1.2 Create a Formation

In this step, you will create a Formation at the Global account level of your SAP BTP account. A Formation is used to connect one or more Systems created in SAP BTP to a specific runtime.

1. Within your global SAP BTP account, choose the `System Landscape > Formations` menu options. Click on the `Create Formation` button.

![Register Formation](./images/4-create-formation.png)

2. Provide a `Name`, choose your `Subaccount` where the Kyma runtime is enabled and select the `System` name you created in the earlier step. Click on `Create`.

![Formation Details](./images/5-formation-details.png)

## Exercise 1.3 Pair an Application

The pairing process will establish bidirectional trust between your CCv2 application and the SAP Kyma runtime. Once the pairing is complete, the registration of APIs and business events can be performed without dealing with explicit authorizations.

1. Navigate back to the CCv2 backoffice and go to `System > API > Destination Targets`. Select the `Default_template` and click on the icon next to the trash-bin to create a new Destination Target.

![Backoffice](./images/6-backoffice.png)

2. Paste the token you copied earlier from the System registration step inside the `Token URL` field and give your connection a name in `Destination's ID`. Click `Register Destination Target` button.

![Backoffice](./images/8-backoffice-registration-sub.png)

**Note**: If you are sharing the CCv2 tenant with another session participant, make sure to add your own name in the `Destination's ID` field.

## Exercise 1.4 Check Connection

Well done! You successfully completed the initial pairing process between CCv2 and Kyma. If everything is running smoothly, you should see the following pages on your own CCv2 Backoffice and BTP systems.

> System - Created Successfully.

![System](./images/9-btp-system-registered.png)

> Formation - Created Successfully.

![Formation](./images/10-btp-formation-registered.png)

> Backoffice - Kyma Registered Sucessfully.

![Backoffice](./images/7-backoffice-registration-done.png)

## Summary

Congratulations, you now have a working Kyma/CCv2 connection and are ready to move into the next exercises.

Continue to - [Exercise 2 - Exploring Exposed Events and APIs](../ex2/README.md)
