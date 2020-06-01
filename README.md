## Task

Create jenkins pipeline which will be executed by trigger with additional requirements 

## Info

Input:

VM with git and app inside /home/project1/

sudo access for ex. user - admin password str0ngpassw0rd (should not be hardcoded in pipeline)

Folder /home/project1/ contains 2 folders  - data and code

project stored in git 

Business requirements - we should trigger this pipeline by webhook and do remote "git pull" in /home/project1 but ONLY if we have some changes in data folder.


 
## Conditions

1. deadline:
    - 2020-05-27 16:00:00
2. tools:
    - Jenkins declarative pipeline 