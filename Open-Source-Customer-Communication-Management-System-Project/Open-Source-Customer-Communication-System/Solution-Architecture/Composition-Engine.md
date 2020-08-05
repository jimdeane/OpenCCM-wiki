# Composition Engine
The Composition Engine is responsible for determining which output items are required to be produced for each External Request that is made. 

Each external request may have associated with it an arbitrary number of output items for example:

| POLICY_WELCOME_PACK  | Email to Policyholder                                                | Welcome email containing a link to the system document repository containing the Policy schedule etc. |
|----------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Email to the advisor | Informing the advisor that the policy welcome pack has been created. |                                                                                                       |
| SMS                  | To the Policyholder confirming the policy created                    |                                                                                                       |
| PDF document         | The policy schedule itself stored in the document repository.        |                                                                                                       |
| POLICY_WELCOME_PACK  | Email to Policyholder                                                | Welcome email containing a link to the system document repository containing the Policy schedule etc. |
| Email to the advisor | Informing the advisor that the policy welcome pack has been created. |                                                                                                       |
| SMS                  | To the Policyholder confirming the policy created                    |                                                                                                       |
| PDF document         | The policy schedule itself stored in the document repository.        |                                                                                                       |

Note, the documents stored in the repository with a link may equally be sent as
attachments to the email(s).

the necessary output format by the rendering engine.
