
::: mermaid
``` mermaid
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
id10[10 Process SMS<br>confirmation<br>of inbound];
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
```
:::
