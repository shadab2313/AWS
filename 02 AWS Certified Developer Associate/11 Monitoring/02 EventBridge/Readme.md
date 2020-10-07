# EventBridge

## Acronym
* SaaS - Software as a Service
* CW - CloudWatch

## Doc

## Intro
* EventBridge is the next evolution of CloudWatch Events
* **Default event bus**: generated by AWS service (CloudWatch Events)
* **Partner event bus**: receive events from SaaS service or applications
    * Zendesk
    * DataDog
    * Segment
    * Auth0...
* **Custom Event buses**: for your own applications
* Event buses can be accedded by other AWS accounts
* **Rules**: how to process the events (similar to CloudWatch Events)

---

## EventBridge Schema Registry
* EventBridge can analyze the events in your bus & infer the **schema**
    * schema = how the data is structured (schema of a DB)
* The **Schema Registry** allows you to generate code for your application, that will know in advance how data is structured in the event bus
* Schema can be versioned

### Screenshot
[<img src="https://i.imgur.com/7Yugiyp.png">](https://i.imgur.com/7Yugiyp.png)

---

## EventBridge vs CW Events
* EventBridge builds upon & extends CW Event
* It uses the same service API & endpoint, & the same underlying service infrastructure
* EventBridge allows extension to add event buses for your custom applications & your third party SaaS apps
* Event Bridge has the Schema Registry capability
* EventBridge has a different name to mark the new capabilities
* Over time, the CW Events name will be replaced with EventBridge