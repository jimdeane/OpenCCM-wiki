
::: mermaid
graph TD;
id00[Registration<br>fa:fa-camera-retro<br>];
id00---id01[Send email<br>confirmation];
id00---id02[Send SMS<br>confirmation];
id00---id03[Send Registration<br>and<br>welcome pack];
id04[something else];
id05---id05[Process email<br>confirmation<br>inbound];
id06[Process SMS<br>confirmation<br>inbound];


class id00 yyy;
classDef yyy fill:yellow,stroke:#333,stroke-width:2px;
linkStyle 0 stroke:#FFF,stroke-width:4px,color:red;
linkStyle 1 stroke:#FFF,stroke-width:4px,color:red;
linkStyle 2 stroke:#FFF,stroke-width:4px,color:red;
linkStyle 3 stroke:#FFF,stroke-width:4px,color:red;
%%linkStyle 4 stroke:#FFF,stroke-width:4px,color:red;
%%linkStyle 5 stroke:#FFF,stroke-width:4px,color:red;

:::
