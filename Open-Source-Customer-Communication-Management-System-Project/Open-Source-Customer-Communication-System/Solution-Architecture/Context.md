# Context

## Background

This document is an outline Architecture Design document for a possible in-house
development of a Customer Communication System that could, at least partially,
provide the functionality of an external vendor’s product such as *Quadient* or
*Open Text*; both of which are, at the time of writing, being considered for
purchase.

## Scope

The external vendors solutions are extremely comprehensive, and their cost
reflects this. In addition, these vendors both have very mature products that
are well tested in the market and are clearly robust and reliable.

An in-house development cannot compete with most of these product properties
however it can provide ‘good enough’ feature coverage and, of course, would be
comprehensively tested.

The scope of the design is intended to provide for the most important elements
of the requirements that were presented to vendors in the Request for Proposal
made to the vendors mentioned above.

## Declaration 

Much of the original design that is the genesis of this proposed design was
created by the author for a previous customer for which the Intellectual
Property (IP) was retained by the author. To the extent that it is revealed in
this document the author makes no claim on that IP and this design may be freely
used by Old Mutual Wealth (OMW) provided no claim is made by OMW on that IP.

The re-use of a previous design has made it possible to provide far more detail
than a normal Solutions Architecture document would be able to do and enables
the provision of an order of magnitude of the potential cost.

## Cost

Section ‎7, Costs(Page 26) provides an outline of the potential costs based on a
previous project of similar nature and an estimate of the nature of the user
stories involved.

## Note

All diagrams in this document are either embedded (Visio) or are extracted from
an ArchiMate Model built using the open source Archi system. This model is
embedded here:

# Solution Context 

## Overview / Vision

The system described in this document is intended to be a partial implementation
of the functionality that is provided by external vendors such as Quadient and
Open Text.

## Future Architecture

The following diagram illustrates how the proposed system would interact with
the current OMW front end systems.

The system as described would be able to be used with any system that can
provide a Data Layer that can aggregate data (see Future Fit Data Layer
Solutions Architecture Document).

![image.png](/.attachments/image-40d753e2-11cc-45ab-b522-08f4a00888f3.png)
## As-Is Architecture

The current reporting and document production systems for the “Front End”, i.e.
customer and advisor facing systems have a simple data architecture that
populates data objects as required for specific output templates.

![image.png](/.attachments/image-451d9ffa-5dbd-446e-98e1-4424353002ff.png)

## Transition Planning

The current system depends on the use of standard tools such as Microsoft word
and proprietary code. There is no expectation that there will be a migration
path from the as is to the to be. Transition will be achieved by completely
reworking the current templates and mechanisms within the to be architecture.

This is certain to be performed in phases that are yet to be defined.

# Architecture Goals and Constraints

## Enterprise Architecture Alignment

The architecture and design of this system follows the requirements of Old
Mutual (OM) Enterprise Architecture.

## Architectural Assumptions and Decisions

The architectural design of the Data Layer has, within Enterprise Architecture
guidelines, been influenced by the Business goals.

No other assumptions or decisions have yet been made.

## Solution Architecture Principles and Constraints

### Principles

![](media/7db47bf9ce0ae8cf6e229575c4c798f3.png)

### Constraints

None so far.

## Solution Architecture Attributes 

### Technology

| **Category**   | **Vendor**  | **Product**                     | **Version**   | **Status** |
|----------------|-------------|---------------------------------|---------------|------------|
| Software       | Microsoft   | .Net                            | Core 2.0      |            |
| Software       | Microsoft   | Entity Framework                | Core 2.0      |            |
| Infrastructure | Microsoft   | IIS                             | 7             |            |
| Infrastructure | Microsoft   | SQL Server                      | 2012 or later |            |
| Infrastructure | Microsoft   | MSMQ messaging                  | 6.3 or above  |            |
| Libraries      | Open Source | GrapesJS <http://grapesjs.com/> | TBA           |            |
|                |             |                                 |               |            |
|                |             |                                 |               |            |

Table - Hardware and Software Technologies

### Pattern

The construction of the data layer will conform to the following architectural
patterns:

-   ASP.NET API 2 RESTful services

-   ASP.NET MVC for administration, monitoring and dashboards.

-   S.O.L.I.D design principles

### Common Services 

**IAM Service**

This solution will make use of the IAM services to authenticate users who
participate.

Authorisation for administrative access will also be performed through IAM
services.

### Common Components

None other than those described in this architecture document.

### Licensing / Commercials?

None, the development of the data layer will be entirely in-house using either
standard Microsoft or appropriately licensed open source libraries requiring no
additional licensing.

### Other Solution Architecture Attributes

None.

## Non-Functional Requirements

### Portability

The design calls for the use of Microsoft .NET Core 2.0 throughout. This
technology may be deployed on Windows and Linux should this be required.

However, some of the infrastructure is currently only supported on Windows (IIS,
MSMQ, SQL Server) and alternatives for these infrastructure elements would have
to be found.

### Capacity and Performance

The system must be able to provide data services that have the capacity to
aggregate data for all the known CCM requirements and be scalable for future
capacity.

### Availability and Reliability

As for the OMW “Front End” systems.

### Scalability

The data layer must be able to scale with the requirements of the current OMW
“Front End” systems.

### System Management, Monitoring, Auditing and Administration

The system must provide the following:

-   Detailed logs of all:

-   Errors

-   Warnings

-   Informational logs

    at configurable levels of verbosity.

-   Provide a dashboard

### BC/DR and COOP

As for the current “Front End” systems.

### Legal and Compliance

None.
