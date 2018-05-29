# Nuxt.js & Strapi.js CMS  Blog

A Tutorial to create a blog with Nuxt.js frontend & Strapi.js CMS backend 

This repo contains the code for a demo blog built with [Nuxt.js](https://nuxtjs.org) & [Strapi.js CMS](https://strapi.io).

## Install Strapi.js
From [Strapi.io](https://strapi.io/getting-started)

Install Strapi:
```bash
$ npm install strapi@alpha -g
```

Create a project:
```bash
$ strapi new myProject
$ > Choose your main database: MongoDB (highly recommended)
$ > Database name: strapi
$ > Host: 127.0.0.1
$ > Port: 27017
$ > Username:
$ > Password:
$ > Authentication database:
$ > Enable SSL connection: false
```

Enter project and Launch Strapi server:
```bash
$ cd myProject
$ strapi start
```


## Build Setup

``` bash
# install dependencies
$ npm install # Or yarn install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout the [Nuxt.js docs](https://github.com/nuxt/nuxt.js) and [Strapi.js docs](https://strapi.io/documentation/).
