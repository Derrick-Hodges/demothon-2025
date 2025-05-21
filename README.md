# demothon-2025
# Artifacts for demothon 2025

## Pretext
>[!Note]
> Teach your grandmother to suck eggs: Emerging sometime in the 1700s, and less commonly used today, this phrase intimates that a person might be "presuming to teach someone something that he or she knows already,"
> ![image](https://github.com/user-attachments/assets/6677dbb4-a612-40be-9044-4aeabebcffc9)

## Introduction
A Solace demo is a precious opportunity to position the full Solace platform as a set of valuable capabilities and should demonstrate the experience of user personas. It should also be alinged to those capabilities and messages in the MGI pitch.  It's also important to pick a use case that is relevant to the audience. This underlines the imprtance of thorough dicovery questioning prior to the demo. No canned demo's!

![image](https://github.com/user-attachments/assets/58e6a90c-e985-4b5f-bf76-e38903d44f53)


To ensure the demo is relaistic the user should leverage public domain respositories for process and semantic alignment to relevant industry.

>[!Note]     
> Examples are
> - TMForum - Telco
> - BIAN - Banking
> - ISA-95 - Industrial processing
> - Local reserve bank - retail banking initiatives such as Payments

There are many more and all are useful.

This repository is used to create Solace NGI demos based on business use case that demo starte the following capabilities

1. Event and application modelling in Event Portal
2. Topic Routing in Event Portal
3. Event Mesh setup
4. Micro Integration Setup
5. Discovery using Event Portal catalouge
6. Event Mesh Runtime
7. Distributed Tracing using OTEL compatible monitoring tool e.e New Relic

## Pre-requisites
- Solace Cloud account with at least 1 service
- Dt allocation to Solace Account, configured and deployed
- Sample messages
- sdkperf JMS version (using auto instrumentation)
- optional collector (for sdkperf)
- scene setting slide

### Example slide to insto the demo

![image](https://github.com/user-attachments/assets/75b50af9-4add-4895-bd78-4f3e218cb1de)



## Methodology
To build a demo the user would follow the process detailed below

![image](https://github.com/user-attachments/assets/964f11fa-cae0-4b97-a6e7-3d4f4206afb8)

### Discovery
Work with your prospects to understand their Business Problems and select a use case that address that area.

### Model
Use EP to model a realistic Topic Hierarchy and model flows to match the use cases. During this stage prepare the runtime environment including mesh configuration and modelled event mesh.

### Deploy
Once modelling is complete deploy to runtime. 

> [!Note]
> Python script being developed to automate this

### Config
Using the sample scripts adapt to the use case. The following parameters will be required
1. service.name=\<service name of micro servce\>
2. connection parameters=\<conenction to PubSub+ Services/>
3. other sdkperf parameters

> [!Note]
> The demo will run on a single node or multi node event mesh

#### Simulation tools
The primary simulation tool is sdkperf. The reason for this is the sdkperf feature 'publish on receive'. This specifically allows the simulated microservices to read messages and subsequently publish messages int he same trace. This leads to much more realistic and interesting traces when demo'ing the DT trace.
If HTTP requests are relevant to the demo I have also used Postman and even curl


