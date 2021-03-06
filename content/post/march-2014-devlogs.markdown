---
layout: post
title: March 2014 Devlogs
date: 2014-03-30 23:57:55.000000000 +05:30
type: devlogs
date: 2014-03-30T00:00:00-00:00
draft: false
---
The month started with plan to learn [Node.js](http://nodejs.org/). With little knowledgable in javascript was very much reluctant or does not have much confident in starting or diving into node.

So initially thought of downloading some ebooks and just follow what they have said.
But later thought let us do it with a simple project.

So my long idea of saving the links I visited to a place for future reference is the project I choosed. But where to start?

Help came in hand with this [link](http://cwbuecheler.com/web/tutorials/2013/node-express-mongo/).

The tutorial has a simple app to store user id and email id in mongo db and retrieve and show to users.

So instead of using that I made my idea live.

Step 1 was installation which I had done a year back with eagerness to learn node. So basic node with npm is already installed.

Step 2 was to install [express](http://expressjs.com/). I learnt that it is web application framework for single and multi page web applications.

`npm install -g express`

Step 3 Create Basic Express application by simple command.
`express --sessions mylinks`

Step 4 Adding the dependencies.
       Whatever I am gonna use it in my application all the related dependencies must be configured here(I have written it under my way of understanding)
Done in the file that is being created as part of express routine.
`package.json`
This was my initial config in package.json
<pre><code>{
  "name": "MyLinks",
  "version": "0.0.1",
  "private": true,
  "scripts": {
    "start": "node app.js"
  },
  "dependencies": {
    "express": "3.4.8",
    "jade": "*",
    "mongodb":"*",
    "monk":"*"
  }
}</code></pre>
Here [monk](https://github.com/LearnBoost/monk) is used for accessing MongoDB from Node.js.

With initial learning about Mongo DB queries using [MongoDB University](https://education.mongodb.com) was easily able to insert and retrieve data from MongoDB collections.

Had the difficulty in understanding the how Node.js application works.

Then got a grap of it. Let me put in my works of understanding.

All the neccesary dependencise will be included using `require`.
An object of `express` is mainly used for routing.
Based on the url with which the object being used the corresponding routes are used and provide the response.
To access the database db objects which are created using monk are passed to the routes function. 
From the routes function corresponding jade which is the layouts being rendered to the users.

With intial Setup and code written I was able to select the data from the db and display. But had issues while displaying with JADE. The indentations made it worse.

Then the next feature of adding links to the db.
Created a simple form using JADE and on submit called a url which inturn has the neccesary the logic to store in db by getting values from the request.

Then added the feature for having tags to the links.
We can store array of mutiple values to a column(field) in MongoDB since it is similar to JSON.

So stored the tags in the way. Retrieving and displaying again got some trouble with JADE. Used for loop to fetch all the links and for each link had a for loop for all the tags within it. Again indentation problem arised but fixed with option in Sublime to convert spaces to indentations.

Now adding the tags had a problem. How the user will add the tags. We cannot be sure of how many tags can a link be associated with. Hence planned to get user input with comma separated. And fetched the field value and split it using commas and store in array and passed to addlink route.
`tags=req.body.tags.split(",")`

Later want to try another driver used for accessing MongoDB from Node.js. It was [mongoskin](https://www.npmjs.org/package/mongoskin).

Modified the package.json
<pre><code>
{
  "name": "MyLinks",
  "version": "0.0.1",
  "private": true,
  "scripts": {
    "start": "node app.js"
  },
  "dependencies": {
    "express": "3.4.8",
    "jade": "*",
    "mongodb":"*",
    "mongoskin":"*"
  }
}
</code></pre>

The db object creation part differs from that of monk.

Also the way in which collections are accessed are also differnt. Hence modified the changes.
Added links between the pages.
My first web application with Node.js,MongoDB,Express and Jade is done.
Find the code in below path
[https://github.com/balaaagi/MyLinks](https://github.com/balaaagi/MyLinks)

Few more features to be added in coming weeks.

It was too slow to complete this learning itself. Hope I pick the pace soon...




