# demothon-2025
## Artifacts for demothon 2025
A demo should position the full Solace platform as a set of valuable capabilities and should demonstrate the experience of user personas. It should also be alinged to those capabilities and messages in the MGI pitch.  It's also important to pick a use case that is relevant to the audience. This underlines the imprtance of thorough dicovery questioning prior to the demo.

To ensure the demo is relaistic the user should leverage public domain respositories for process and semantic alignment to relevant industry.
[!TIP]
Examples are
TMForum - Telco
BIAN - Banking
ISA-95 - Industrial processing
Local reserve bank - retail banking initiatives such as Payments

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
- Sample messages
- sdkperf JMS version (using auto instrumentation)
- optional collector (for sdkperf)

## Methodology
To build a demo the user would follow the process detailed below

![image](https://github.com/user-attachments/assets/964f11fa-cae0-4b97-a6e7-3d4f4206afb8)

### Discovery
Work with your prospects to understand their Business Problems and select a use case that address that area.

### Model
Use EP to model a realistic Topic Hierarchy and model flows to match the use cases. During this stage prepare the runtime environment including mesh configuration and modelled event mesh.

### Deploy
Once modelling is complete deploy to runtime. 

[!NOTE]
Python script being developed to automate this

### Config
Using the sample scripts adapt to the use case. The following parameters will be required
1. service.name=<service name of micro servce>



## Simulation tools
