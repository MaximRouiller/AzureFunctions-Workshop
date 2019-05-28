---
title: "What is serverless?"
weight: 101
outputs: ["Reveal"]
---

## What is Serverless?

- Execution model
- Pay as you consume
- No need to control scaling

{{% note %}}
Serverless is an execution model. Everytime you hear the word serverless, it's talking about this cloud focused execution model. Running the same code locally is a different concept.

An attribute of that execution model is that you pay for what you consume and not for what you reserve. When you create services in cloud providers, you reserve for a certain amount of CPU/RAM. This is not a necessary concern when you start a new serverless application.

Serverless goes without this as the whole premise to care about servers less. Meaning that when using a serverless framework, you should not be required to control scaling at all.

Now, how do you run code on a Serverless platform? This takes us to...

{{% /note %}}

---

## Serverless Runtime

Available Runtimes:

- Azure Functions
- AWS Lambda
- Google Cloud Functions
- IBM Cloud Functions
- ...

Also called Functions as a Service (**FaaS**)

{{% note %}}

The runtime. The runtime is the code behind that runs your code. Every cloud provider offers their own but what is important to note is that it's different from Serverless. Those runtime may allow you to run your code locally or in an orchestrator.

{{% /note %}}

---

### Azure Functions as a Serverless Runtime

- Azure Functions is the Runtime
- Azure Functions Consumption Plan is Serverless
- Every Azure Functions can run locally, in the Cloud, and on Kubernetes  

{{% note %}}

What interests us today is Azure Functions. Functions is the Microsoft FaaS implementation and using the Consumption Plan on Azure is the serverless implementation.

{{% /note %}}
