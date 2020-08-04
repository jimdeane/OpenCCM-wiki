# Open Source Customer Communication System


Ernaspark Ltd has a need to centralize and rationalize the customer communications that are made both to and from the core systems and from staff directly communicating with customers. 

There are several commercial  Customer Communication (CCM) systems that are capable, but expensive. Therefore Ernaspark have decided to sponsor an Open Source development that this open source system will emulate the capabilities of these systems to the extent that they are required by Ernaspark.  

One of the primary design principles is to provide total separation of the CCM from the “legacy” system, with extremely clearly defined interfaces for requesting outbound communications and being informed of inbound. 

The business requirement is show in an overview diagram as follows:

![FeatureBlockDiagram.png](/.attachments/FeatureBlockDiagram-51b86914-94aa-40a5-83c1-d638d7e94fb6.png)

The components are briefly described here:

## Core Business Systems
Ernaspark's core business systems that will be initiating communication using the new systems and receiving notifications of responses from customers. The new system will be accessed using a set of well-defined Application Programming Interfaces (APIs) as well as exposing mechanisms that will allow the new system to notify the core of responses, where these are to be expected. 

## Core Business Customisations
OpenCCM will expose three categories of customisation points that Ernaspark can provide customisation code for. These customisations are provided by Ernaspark as .NET Core libraries (DLLs) that OpenCCM calls in specified circumstances (according to the OpenCCM parameters). The categories provided for are:
### Data Services

### Custom Rules

### Custom Code

