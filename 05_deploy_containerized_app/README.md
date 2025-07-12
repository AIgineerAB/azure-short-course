# Dockerize an application and push it to Azure Container Registry

- dockerize a react app
- push the image to Azure Container Registry
- pull the image from Azure Container Registry into Azure App Service

<a href="https://youtu.be/L7xfKPQLgTA" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/azure/react_deploy_web_app.png?raw=true" alt="DESCRIPTION" width="600">
</a>


## Create react app
```bash
npm create vite@latest my-app -- --template react
```

Installing dependencies:
```bash
cd my-app
npm install
```

Run development server to check it works:
```bash
npm run dev
```

Now build the distribution:
```bash
npm run build
```

## Nginx configuration

Create a file named `nginx.conf` in the root of your project with the following content:

```nginx
events {}

http {
  include       mime.types;
  default_type  application/octet-stream;

  server {
    listen 80;
    server_name localhost;

    root /usr/share/nginx/html;
    index index.html;

    location / {
      try_files $uri $uri/ /index.html;
    }
  }
}
```

## Dockerize 

Create a `Dockerfile` in the root of your project with the following content:

```dockerfile
FROM nginx:alpine

RUN rm -rf /etc/nginx/conf.d

COPY nginx.conf /etc/nginx/nginx.conf

COPY dist/ /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
```

build the docker image and spin up the container:

```
docker build -t <image_name> .  
docker run -p 8080:80 <image_name>
```

## Push to Azure Container Registry (ACR)

```bash
docker login <your-acr-name>.azurecr.io
docker tag <image_name> <your-acr-name>.azurecr.io/<image_name>
docker push <your-acr-name>.azurecr.io/<image_name>
```

## Mac arm-based (M-chip)

Building docker image on mac arm-based machine will generate an image that is not compatible with Azure Web App for Linux as it uses a different architecture (linux/amd64). The solution is to build the image using `buildx` which allows you to specify the platform.


```bash
docker buildx create --use
docker buildx ls # to check the platforms
docker buildx inspect --bootstrap
``` 

Now before we use buildx to build for amd64 and arm64, we build an image locally first and spin up the container as you would usually do:

```bash
docker build -t <your-image-name> .
docker run -p 8080:8080 <your-image-name>
```

Lets log into azure container registry (ACR) and provide the login credentials:

```bash
docker login <registry-name>
```


Now that it works we can build the image for multiple platforms and push it to Azure Container Registry (ACR):

```bash
docker buildx build --platform linux/amd64,linux/arm64 -t <acr_login_server>/<name>:<tag> --push .
```




## Other videos 📹

## Read more 👓
