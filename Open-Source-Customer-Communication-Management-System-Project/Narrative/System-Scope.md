## System Overview

The scope of the system is based on this:

<div style="background-color: lightgrey;">

###Taken from a Financial Services, Life and Pensions, Fintech
ecosystem that can lead to communications of various sorts

####Registration
-   Send email confirmation
-   Send SMS confirmation
-   Send Registration details / welcome pack
-   Process email confirmation inbound
-   Process SMS confirmation inbound
 
####New Business Policy Servicing
-   Send a quote document
-   Underwriting
    -   Send an underwriting special terms letter
    -   Process customer acceptance or rejection of terms
-   Policy fulfilment
    -   Send welcome pack
    -   Send Policy Details

####Business Architectural
-   Access must be controlled to all features
-   Communications types must include
    -   Printed media (via PDF)
    -   Emails
    -   Text Messaging
        -   SMS
        -   WhatsApp
        -   Signal
        -   Telegram
        -   Others as they become mainstream
    -   Social Media
        -   Facebook
        -   Instagram
-   All communications stored in a historical database accessible to business
    and customers.
-   Version histories of all artifacts must be kept
-   Define a process flow for the sending and receiving of communications
-   Define Rules that can direct wherever
-   Require certain communications to be approved by nominated parties according
    to rules before distribution
-   Create and maintain templates for all communications made
-   Define the composition of the communications made for any core busines event
-   Create ad-hoc business events
-   Map core business events to communications events
-   Map core business objects / values to communication objects / values
-   Correlate inbound communications with outbound communications where
    applicable
 
####Technical Architecture and process
-   Microsoft architecture; .NET Core, SQL Server (etc.)
-   Queueing architecture to ensure scalability and performance (RabbitMQ)
-   Browser based UI for all components
-   Azure hosting
-   Azure DevOps ADLC
-   Agile process
-   ATDD, BDD, TDD techniques throughout
-   Command Query Responsibility Separation (CQRS) design
-   Micro Services
<br>

 </div>