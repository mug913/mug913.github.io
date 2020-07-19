---
layout: post
title:      "the Fetch API"
date:       2020-07-19 19:04:13 +0000
permalink:  the_fetch_api
---

One of the most crucial components of my recent JS project is the fetch() method. This method has deceptively simple code pattern and is easy to learn by rote, but let’s take a closer look at the steps involved to try a get a sense of its full functionality. 

The first part is the calling of the fetch itself, passing in the URL and returning a promise object. What is a promise object? Well a promise is a special type of object which is meant to represent the status of an asynchronous operation. Of note, it can be chained with .then blocks, which themselves will contain the callback function to be run when the original method completes (and the promise is resolved). How are they themselves chain-able? Well .then methods themselves return promises, so the the wait/respond functionality can continue on and on.

So we make our fetch, passing in an URL and receiving back the promise. This promise is resolved with an object when the network call finishes and the URL delivers what is called a body object. This object will allow us to access the Response stream containing our data, which is not immediately accessible in this form. Thankfully, the body objext also has some basic functions included in it allowing for processing the response stream of our data into a readable form. This is where the .then comes in, as we can use this method to utilize one of these functions (.json, .text, etc..) and return the result. Now thanks to the chain-able nature of the .thens discussed above, we can attach another callback function to utilize this data however we intended. All in a series of readable asynchronous code.

There are more advantages to using the Fetch API, such as the simplified error handling that comes along with it’s use of promises, that are worth diving into, but I hope this gives a little more clarity as to what is occurring when using a fetch() method. 


