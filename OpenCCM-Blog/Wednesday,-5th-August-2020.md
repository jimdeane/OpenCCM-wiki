## Why a blog
Decided today that I need to keep track of what is happening in this project outside of:

- the project itself
- the narrative and
- my own personal journal

I think this is important as the the other project areas in the Wiki serve particular purposes in relation to the development of the project itself while my personal journal is about me and not the project. 

I'm therefore going to try to keep this up to date to record what I do on the overall project, when things happen and generally report on its progress. 

## Catch-up

After deciding to create this project as an illustration of capabilities in the search for a "new" career in software development I have:

- come up with the subject of the project ( the OpenCCM system )
- Built the very basic infrastructure that will be required to do the development within the Azure DevOps ecosystem and started to pull together the necessary bits and pieces, which to start wit hare:
    - Git repo for the code with a template .NET Core project in it
    - This WIKI
    - Build pipelines for:
        - A Continuous Integration (CI) build step for the .NET Core project
        - A CI build step to synchronize the code repo with a GitHub mirror. This to enable GitHub browsers to see what I'm doing and to provide a direct GitHub link.
        - A CI build step to synchronize the WIKI repo with a GitHub mirror. 
    - added the necessary additions to integrate SpecFlow and, SpecFLow+ LivingDoc to the DevOps infrastructure.
    - Created a little dashboard to bring all of this together.



