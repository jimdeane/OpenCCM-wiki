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
Data Services provide an API for OpenCCM to discover the data it needs to use to satisfy outbound communications. 

### Custom Rules

OpenCCM  evaluates rules in many places to determine what communication to make and to tailor the communication itself. In many cases this can be done with the built in configurable rules, however, in some cases it is either easier to or necessary to have more complex rules and these can be written in any .NET language and called by OpenCCM when required.

### Custom Code

As well as calling out for custom rule evaluation OpenCCM has opportunities for calling out to custom code, written in a .NET language, to override or compliment the processing available in the standard system. 

## OpenCCM Core

The OpenCCM Core orchestrates each of the feature modules to perform the required processing.

## Access Management

## Authoring

## Repository

## Versioning

## Pre-Render Editing

## Rendering

## Composition

## Correlation

## Outbound Distribution

### Email

### Text Messaging

### Physical Media

### Social Media 

#### Facebook

#### WhatsApp

#### Web Consumer

#### PDF Consumer

#### Text Consumer

## Inbound Routing

