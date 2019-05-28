---
title: "What is serverless?"
weight: 101
outputs: ["Reveal"]
---

## What is Serverless?

- Execution model
- Pay as you consume
- No need to control scaling
- Event Driven

{{% note %}}
Serverless is an execution model. When you hear the word "serverless", it's talking about a cloud-focused execution model. Running the same code locally is a different concept.

An attribute of that execution model is that you pay for what you consume and not for what you reserve. When you create services in cloud providers, you reserve for a certain amount of CPU/RAM. This is not a necessary concern when you start a new serverless application.

Serverless goes without this as the whole premise to care about servers less. Meaning that when using a serverless framework, you should not be required to control scaling at all.

Finally, everything in serverless is in someway related to events. Whether we are talking about an HTTP request, a timer, a new file is added to a cloud storage, or a message to unqueue, it's all concepts found in serverless. Those events allow the Cloud provider to detect when it needs to provision more or less resources for your application.

Now, how do you run code on a Serverless platform? This takes us to...

{{% /note %}}

---

## Serverless Runtime

Available Runtimes:

- Azure Functions
- AWS Lambda
- Google Cloud Functions
- IBM Cloud Functions
- OpenFaaS
- ...

Also called Functions as a Service (**FaaS**)

{{% note %}}

The runtime. The runtime is the code behind that runs your code. Every cloud provider offers their own but what is important to note is that it's different from Serverless. Those runtime may allow you to run your code locally or in an orchestrator.

{{% /note %}}

---

## Azure Functions as a Serverless Runtime

- Azure Functions is the Runtime
- Azure Functions Consumption Plan is Serverless
- Every Azure Functions can run locally, in the Cloud, and on Kubernetes  

{{% note %}}

What interests us today is Azure Functions. Functions is the Microsoft FaaS implementation and using the Consumption Plan on Azure is the serverless implementation. Every Function that you write today will run on your local machine as well as in the Cloud.

{{% /note %}}

---

## Why Serverless?

{{% note %}}

So now that we know what serverless is, why use it? Why not just create a single VM and go from there?

{{% /note %}}
---

## Why Serverless?

### Advantages

- Cost
- No concern about scaling, the cloud takes care of it
- Simplified development model

{{% note %}}
Let's start with the obvious. Cost. Since resources are not reserved, you are only getting invoiced for what you are using and most cloud providers offer you a free quota.

This allows you to build an application without using a single virtual machine. A minimum viable product can be hosted for less than the cost of the milk you put in your coffee.

Then, without having to care about scaling and letting your cloud provider take care of it, you can keep on focusing on your application instead of on the infrastructure.

Finally, the simplified development model means that you work on smaller/simpler units. Meaning that your code is simpler to work, deploy, and scale.

So, to all advantages... we must bring the other side of the coin.
{{% /note %}}

---

## Why Serverless?

### Disadvantages

- Cold-start/Performance
- Simplified development model
- 
- Potential Vendor Lock-in

{{% note %}}
Among the disadvantages of running serverless workloads includes Cold-Start/Performance.

Running purely in a consumption plan where you can scale all the way down to 0 servers means that your application could be restarting from scratch with nothing in memory. Hence the `cold-start` meaning. Azure solves this partially by allowing an hybrid of consumption and reserved compute which we can talk about later.

With a simplified development model brings its own issues. Things being simpler means that you can't tweak and customize everything as easily as if you had 100% control of the application.

Finally, each vendor has their own implementation meaning that every application built with this model is at least lightly tied to the vendor that you use.
{{% /note %}}
