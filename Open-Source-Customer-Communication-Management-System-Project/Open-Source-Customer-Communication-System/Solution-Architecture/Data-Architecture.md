# Data Architecture

## Data Model

The following diagram illustrates the important parts of the data model used for
this design:

![image.png](/.attachments/image-2a568971-ac70-4dd1-9d5e-9c5f961bcaed.png)

The entities in this model are as follows:

| Entity                                     | Description                                                                                                                                                                                                                                                                                                |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workflow                                   | This table holds all of the allowable types of External Request that may be made of threw system for the production of output items. An example would be POLICY_WELCOME_PACK which may produce an email, several pages of policy schedule, an alerting SMS as well as an informative email to the Advisor. |
| WorkflowAction                             | This table provides for multiple steps to be defined for a workflow. For example, where a message sent normally awaits a reply the result of receiving the reply may be defined as a step.                                                                                                                 |
| EventType                                  | There is one to one relationship between WorkflowAction and EventType.                                                                                                                                                                                                                                     |
| DocumentTypeForEventType                   | This table lists, for each EventType, the DocumentTypes that are to be produced for that event type.                                                                                                                                                                                                       |
| NotificationTypeForEventType               | This table lists, for each EventType, the NotificationTypes that are to be produced for that event type.                                                                                                                                                                                                   |
| DocumentType                               | The DocumentType defines the formatting and output type. This definition holds, for example:                                                                                                                                                                                                               |
| NotificationType                           | Notifications describe the type(s) of notifications, for example, SMS or email required to be sent. The content of the notification is defined with its own DocumentType and the mechanism for delivering the notification, for example SMS provider is also defined.                                      |
| AttachementForNotificationTypeAndEventType | Notifications may have attachments and this table defines the DocumentType(s) for each NotificationType that nay be attached. Only allowed for emails.                                                                                                                                                     |
| DocumentRequestLog                         | A log of all requests made.                                                                                                                                                                                                                                                                                |
| DocumentRequestStatusType                  | Internal look-up table                                                                                                                                                                                                                                                                                     |
| InteractionStatusType                      | Internal look-up table                                                                                                                                                                                                                                                                                     |
| InteractionSubType                         | Internal look-up table                                                                                                                                                                                                                                                                                     |
| InteractionType                            | Internal look-up table                                                                                                                                                                                                                                                                                     |
| InteractionTypeForInteractionSubType       | Internal look-up table                                                                                                                                                                                                                                                                                     |
| NotificationRequestStatusType              | Internal look-up table                                                                                                                                                                                                                                                                                     |
| SnapshotType                               | Internal look-up table                                                                                                                                                                                                                                                                                     |
| TransportType                              | Internal look-up table                                                                                                                                                                                                                                                                                     |
| WorkflowActionAssignedToType               | Internal look-up table                                                                                                                                                                                                                                                                                     |
| WorkflowActionCompletionType               | Internal look-up table                                                                                                                                                                                                                                                                                     |
| ClientInteraction                          | A log of every external output made and its relationship to requests made along with the status of the output success.                                                                                                                                                                                     |
| Document                                   | A record of every document output produced along with a reference to the actual output stored for later retrieval.                                                                                                                                                                                         |
| DocumentRequest                            | A log of every document processed.                                                                                                                                                                                                                                                                         |
| Event                                      | A log of every event processed. Events are recorded as a result of WorkflowActions being processed.                                                                                                                                                                                                        |
| NotificationRequest                        | A log of every notification processed.                                                                                                                                                                                                                                                                     |
| NotificationRequestLog                     | A log of the progress of delivering notifications.                                                                                                                                                                                                                                                         |
| Snapshot                                   | The data retrieved from the external system that was used to process the notification or document.                                                                                                                                                                                                         |

-   Master Template name

-   The output type to be rendered

-   The data required for the document to be retrieved from the calling system.

## Authoritative Data Sources

The system depends on two sources of data:

-   The internal reference data and tables described in the data model above AND

-   The data that is supplied through the External App Gateway
