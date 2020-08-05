# Rules and Rules Engine 

There are three types of rules that the system is specified to cater for:

-   Rules embedded in a template, for example a rule that defines whether a block in a template should be rendered.

-   Rules that are common among many templates and are defined separately and outside of any template.

    Embedded rules are always defined using a Rule Builder such as:

![image.png](/.attachments/image-f0f3871f-2194-4880-8d53-8b110bce25e0.png)
  
Common rules are defined as C\# expressions and are stored as custom code and may be referred from anywhere that a rule is required.