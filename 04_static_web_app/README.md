# Simple deployment of React into static web app

<a href="https://youtu.be/_Xw4Uta7r_k" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/azure/static_web_app_react.png?raw=true" alt="deploy react to static web app" width="600">
</a>



## Setup react application

steps: 

1. [install node.js and npm](https://nodejs.org/en/download) if they are not installed 
2. Check versions 

```bash
node -v 
npm -v 
```

3. Create new react app

```bash
npx create-react-app demo-react-app
```

4. cd into demo-react-app and run 

```bash
npm start
```

to start your react app 

5. Now code your awesome application 


## Create Azure Static Web App

Search for the resource Static Web App in Azure portal and then click create resource. Here you choose either an existing resource group or click a new one, choose a name, plan type, then choose to connect to your github and find the repo with your react application. 

<img src="https://github.com/kokchun/assets/blob/main/azure/static_web_app/create_1.png?raw=true" alt="create 1" width="600">


<img src="https://github.com/kokchun/assets/blob/main/azure/static_web_app/create_2.png?raw=true" alt="create 2" width="600">

Choose github for authorization policy and then click review and create

<img src="https://github.com/kokchun/assets/blob/main/azure/static_web_app/authorization_policy.png?raw=true" alt="authorization policy" width="600">

Click go to resource 

<img src="https://github.com/kokchun/assets/blob/main/azure/static_web_app/go_resource.png?raw=true" alt="go to resource" width="600">


Inside the resource you'll find your domain, go there and share your beautiful react app to friends and family :D 

<img src="https://github.com/kokchun/assets/blob/main/azure/static_web_app/view_app.png?raw=true" alt="vist site" width="600">


## Other videos 📹

## Read more 👓

- [What is Azure Static Web Apps - microsoft learn](https://learn.microsoft.com/en-us/azure/static-web-apps/overview)
- [Azure static web app](https://azure.microsoft.com/en-us/products/app-service/static)