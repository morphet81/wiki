# How to use custom private npm modules in Azure

When deploying a NodeJS app on Azure as an App Service, it's very useful to allow deploying from Git: you can them
simply push to Azure in order to deploy you app.

Therefore, if your application uses custom module hosted privately on Bitbucket or github, Azure needs to have the right
to clone the repositories of these modules.

To do so, follow these steps:

1. Open the page ```https://appname.scm.azurewebsites.net/api/sshkey?ensurePublicKey=1``` were 'appname' is the name of 
your app on Azure. You will obtain an RSA key.

2. Follow the steps in [this page](./git-ssh.md) to add the key to your repository account.