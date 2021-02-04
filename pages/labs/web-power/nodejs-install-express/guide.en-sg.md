---
title: Install Express on your POWER web hosting plan
slug: nodejs-install-express
excerpt: Find out how to install Express  on your POWER web hosting plan
section: Node.js
order: 1
---


<style>
 pre {
     font-size: 14px;
 }
 pre.console {
   background-color: #300A24; 
   color: #ccc;
   font-family: monospace;
   padding: 5px;
   margin-bottom: 5px;
 }
 pre.console code {
   border: solid 0px transparent;
   font-family: monospace !important;
 }
 .small {
     font-size: 0.75em;
 }
</style>

**Last updated 3<sup>rd</sup> February 2021**

## Objective

You've subscribed to a Web POWER web hosting plan to deploy **Node.js** applications, and you want to begin developing your project using [Express](https://expressjs.com/).

This guide will explain how to deploy a simple *Hello World* server on Express.


**Find out how to install Express on your POWER web hosting plan.**


## Requirements

- A [Node.js](https://labs.ovh.com/managed-nodejs) POWER web hosting plan
- Access to the [OVH Control Panel](https://www.ovh.com/auth/?action=gotomanager)

If you have just started to use your Web POWER web hosting plan, we suggest you to have a look to our [Getting started with a POWER web hosting plan](../getting-started-with-power-web-hosting/) guide before going further.

## Instructions


Let's suppose you have the default configuration for Node.js hosting:

- Runtime : nodejs 14   
- Entrypoint : index.js 
- DocumentRoot : www

> [!primary]
>
> To verify your configuration, you can use the [Retrieve active configuration](../getting-started-with-power-web-hosting/#api-get-active-configuration) API endpoint

[Access via SSH](../getting-started-with-power-web-hosting/#ssh) to your POWER web hosting, and install Express using `npm`:

```sh
npm install express --save
```

Then go to the `www` folder and create and `index.js` file there:

`index.js`
```javascript
const express = require('express');
const port = 3000;
const msg = `Hello World from NodeJS ${process.version}\n`;
const app = express();app.get('/', function (req, res) {
res.send(msg);
});
app.listen(port);
```

And [restart your instance](../getting-started-with-power-web-hosting/#restart), your Express *Hello World* will be online.

![Express Hello World](images/nodejs-install-express-01.png){.thumbnail}

Terminal output:

<pre class="console"><code>~/www $ cd www
~/www $ node -v
v14.13.0
~/www $ npm install express --save
~/www $ vi index.js
const express = require('express');
const port = 3000;
const msg = `Hello World from NodeJS ${process.version}\n`;
const app = express();app.get('/', function (req, res) {
res.send(msg);
});
app.listen(port);
~/www $ mkdir -p tmp
~/www $ touch tmp/restart.txt</code></pre>

## Going Further

Join our community of users on [https://community.ovh.com/en/](https://community.ovh.com/en/).

**Join [our Gitter room](https://gitter.im/ovh/power-web-hosting) to discuss directly with the POWER Web Hosting team and the other users of this lab**