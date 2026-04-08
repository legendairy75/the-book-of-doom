## Updating
---
change log should be checked before updating gitea to make sure there are no breaking changes. The currently running version of gitea should then be backed up including:
-  database
- config
- data-files in *APP_DATA_PATH*
Gitea should also be stopped before hand. after all of that you can update, restart the service, and your finished!
To see oficial documentation go [here](https://docs.gitea.com/installation/upgrade-from-gitea)
