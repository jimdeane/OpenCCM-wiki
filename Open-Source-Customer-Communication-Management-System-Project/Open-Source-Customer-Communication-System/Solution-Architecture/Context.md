# Solution Context 

## Overview / Vision

The system described in this document is intended to be a partial implementation of the functionality that is provided by external vendors such as Quadient and Open Text.

## Future Architecture

The following diagram illustrates how the proposed system would interact with the Ernaspark Core systems.

The system as described would be able to be used with any system that can provide a Data Layer that can aggregate data (see Future Fit Data Layer Solutions Architecture Document).

![image.png](/.attachments/image-40d753e2-11cc-45ab-b522-08f4a00888f3.png)




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


