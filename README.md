# CA_bootcamp_docker_project

<center>
<img src="https://media.licdn.com/dms/image/D5612AQGUrOgPswOr5w/article-cover_image-shrink_600_2000/0/1690626217523?e=2147483647&v=beta&t=98JZHSFiS9ZJYyL7USObHeWEBeyOVug4gCSZ__XrJKI" />
</center>


This project is a guide for deploying modern web apps with docker. It contains two types of projects; only one technology based ones and multiservices projects.

---
**First of all, make sure to have docker and docker compose correctly installed on your computer !!**

---

## 1. How to deploy web simple modern web apps with docker?
This section of the documentation concerns the following technologies based projects:

### Vue JS (Vue folder)


<center>
<img src="https://static-00.iconduck.com/assets.00/vue-icon-512x439-f6q4zral.png" />
</center>


To deploy a vue app with docker, you first have to create a vue project. You can do so with the following command or any equivalent that you prefer :

```
npm create vue@latest <project-name>
```

Once the project created, copy the Dockerfile located at './Vue/Dockerfile' and place it at the root of your vue project. You'll then be able to create the docker image of your app. You do this, run :

```
docker build -t <image-tag> . 
```
(If you prefer you can place the Dockerfile wherever you want...Just make sure to replace the '.' and the end of the command by the correct relative path.)

Now that your app image is built with docker, you can run it as a docker container with the following command (or directly with docker desktop interface if you have it installed on your machine) : 

```
docker run --name <you-container-name> -d -p <available-port-on-your-machine>:<the-port-your-vue-project-is-set-to-run-on(5173 default)> <image-tag>
```

A good example is :

```
docker run --name my_vue_container -d -p 5173:5173 my_vue_app
```

You can stop the container with : 

```
docker stop my_vue_container
```


### React JS (React folder)


<center>
<img src="https://miro.medium.com/v2/resize:fit:1200/1*y6C4nSvy2Woe0m7bWEn4BA.png" />
</center>


As for the vue case, you  first have to create a react project. You can do so with the following command or any equivalent :

```
npx create-react-app <project-name>
```

Copy the Dockerfile located at './React/Dockerfile' and place it at the root of your vue project. Run :

```
docker build -t <image-tag> . 
```

Now run the image with docker run. 

Here is an example

```
docker run --name my_vue_container -d -p 5173:5173 my_react_app
```


### Nuxt JS (Nuxt folder)


<center>
<img src="https://vueschool.io/storage/media/677bbaa8ba92bed432f2bc7b6490c03a/Nuxt-3-Fundamentals_transparent.png" />
</center>


Create a nux project by running:

```
npx nuxi@latest init <project-name>
```

Copy the Dockerfile located at './Nuxt/Dockerfile' and place it at the root of your vue project. Run :

```
docker build -t <image-tag> . 
```

Now run the image with docker run. 

Here is an example

```
docker run --name my_vue_container -d -p 5173:5173 my_react_app
```




