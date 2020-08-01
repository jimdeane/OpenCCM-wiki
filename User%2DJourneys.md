
::: mermaid
graph TD;
id00[00 Registration<br>fa:fa-camera-retro<br>];
id01[01 Send email<br>confirmation];
id02[02 new thing<br><br>];
id03[03 Send SMS<br>confirmation];
id04[04 Send Registration<br>and<br>welcome pack];
id05[05 something else<br><br>];
id06[06 Process email<br>confirmation<br>inbound];
id07[07 Something<br>under 06]
id08[08 Something else<br>under 06]
id09[09 Another one<br>under 06]
id10[10 Process SMS<br>confirmation<br>inbound];
id00---id01
id01---id02
id02---id03
id04---id05
id05---id06
id06---id07
id06---id08
id06---id09
class id00,id01,id02,id03,id04,id05,id06,id07,id08,id09,id10 sticky;
classDef sticky fill:yellow,stroke:#333,stroke-width:2px;
linkStyle 0 stroke:#FFF,stroke-width:4px,color:red;
linkStyle 1 stroke:#FFF,stroke-width:4px,color:red;
linkStyle 2 stroke:#FFF,stroke-width:4px,color:red;
linkStyle 3 stroke:#FFF,stroke-width:4px,color:red;
linkStyle 4 stroke:#FFF,stroke-width:4px,color:red;
linkStyle 5 stroke:#FFF,stroke-width:4px,color:red;
linkStyle 6 stroke:#FFF,stroke-width:4px,color:red;
linkStyle 7 stroke:#FFF,stroke-width:4px,color:red;
:::

User journeys taken from a Financial Services, Life and Pensions, Fintech ecosystem that can lead to communications of various sorts

Registration
	- Send email confirmation
	- Send SMS confirmation 
	- Send Registration details / welcome pack
	- Process email confirmation inbound
	- Process SMS confirmation inbound

New Business
	- Send a quote document 
	- Underwriting 
		○ Send an underwriting special terms letter
		○ Process customer acceptance or rejection of terms
		
	- Policy fulfilment 
		○ Send welcome pack
		○ Send Policy Details
		
Policy Servicing 
	- Add benefit
		○ Send Quote document
		○ Process customer response
		○ Send revised Policy Details
	
	- Remove benefit 
		○ Send Quote document
		○ Process customer response
		○ Send revised Policy Details
		
	- Premium Collection
		○ Send Debit notification
		○ Send payment reminder

 Business Architectural
	- Access must be controlled to all features 
	- Communications types must include
		○ Printed media (via PDF)
		○ Emails
		○ Text Messaging
			§ SMS
			§ WhatsApp
			§ Signal
			§ Telegram
			§ Others as they become mainstream
		○ Social Media
			§ Facebook
			§ Instagram
	- All communications stored in a historical database accessible to business and customers.
	- Version histories of all artifacts must be kept
	- Define a process flow for the sending and receiving of communications
	- Define Rules that can direct wherever
	- Require certain communications  to be approved by nominated parties according to rules before distribution
	- Create and maintain templates for all communications made
	- Define the composition of the communications made for any core busines event
	- Create ad-hoc business events
	- Map core business events to communications events
	- Map core business objects / values to communication objects / values
	- Correlate inbound communications with outbound communications where applicable

Technical Architecture and process
	- Microsoft architecture; .NET Core, SQL Server (etc.)
	- Queueing architecture to ensure scalability and performance (RabbitMQ)
	- Browser based UI for all components
	- Azure hosting
	- Azure DevOps ADLC
	- Agile process
	- ATDD, BDD, TDD techniques throughout
	- Command Query Responsibility Separation (CQRS) design 
	- Micro Services 
	




