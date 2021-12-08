# 3. Fetch Api for Beginners

The Fetch Api provides a modern interface that allows us to make asynchronous HTTP requests from web browsers to server. If the above sentence doesn't make sense just yet then don't worry. It makes sense as you work more with it. 

Here some resources will be provided which you can use to understand it better. But for this project we will using be the Fetch Api **only** to make basic fetch requests to some third party public apis and get some cata data from their servers. (a third party api is an api provided by somebody else [read more here](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Third_party_APIs)).

So, first of all we will look at the code to fetch cat data using those third's party Apis. Before going ahead you are recommended to watch [this video](https://www.youtube.com/watch?v=cuEtnrL9-H0) at least till 4:00 minutes for better understanding about fetching the data using Fetch Api.

### Cat Facts Api - Base url is https://cat-fact.herokuapp.com    
##### (for documentation visit [here](https://alexwohlbruck.github.io/cat-facts/docs/endpoints/facts.html))   
Note - A base url is the main part of the api url. After that several endpoints, paramteres might be there in the url.

#### Fetch a single cat fact

```js
// fetch a single cat fact
// (here /facts is an endpoint that gives us facts(by default 4 facts) and /facts/random gives back one random fact)
        fetch("https://cat-fact.herokuapp.com/facts/random")
        .then((res)=> res.json())
        .then((data)=>{
            console.log(data)
            /* here the data(a single cat fact) fetched using the api 
            is in the form of object, you can visualize it in the browser console*/
        })
 ```
 
 #### Fetching multiple cat facts
 here we use the **`amount`** parameter provided by the api to
 request multiple cat facts.
 
 ```js
 // fetch a single cat fact
        fetch("https://cat-fact.herokuapp.com/facts/random?amount=10") 
        .then((res)=> res.json())
        .then((data)=>{
            console.log(data)
            /* here the data is an array you can visualize it in the browser console */
        })
 ```
 
 ### Cataas Api - Base url is https://cataas.com/cat   
 ##### (for documentation visit [here](https://cataas.com))
 
 #### Fetching an image url
 ```js
 // fetch a cat image url
        fetch("https://cataas.com/cat?json=true") 
        .then((res)=> res.json())
        .then((data)=>{
            console.log(data)
            /* here the url property of data can be accessed by using data.url syntax(dot notation) since data is an object.
            If you visualize the data.url property in browser conosle you will notice that the provided url is partial 
            and we have to use https://cataas.com/ in front of it to make it complete */
            console.log(`The complete url is https://cataas.com/${data.url}` )
        })
 ```
 
 #### Fetching a cat image url with some text written on the image
 here the api provides us an endpoint **`/says/:text`** which we can use to retrieve a cat image with some text on it  
 for example visit this url - https://cataas.com/cat/says/wow. Explore the api docs for more such interesting endpoints
 
 ```js
 // fetch a cat image with some text on it
        fetch("https://cataas.com/cat/says/wow?json=true") 
        .then((res)=> res.json())
        .then((data)=>{
            console.log(data)
            /* here the url property of data can be accessed by using data.url syntax since data is an object.
            If you visualize the data.url property in browser conosle you will notice that the provided url is partial 
            and we have to use https://cataas.com/ in front of it to make it complete */
            console.log(`The complete url is https://cataas.com/${data.url}` )
        })
```
 
 Once you have the url you can use that url in the src property of image and display the image on your project website.
 
 If you want to see more about how you can do this in a live website and show the data on a webpage then refer this [example website code](https://github.com/konoha-developers/project-neko/blob/main/scripts/main.js).
 
  
## Note - 
1) You only need to know the basic usage of the Fetch Api for this project which is already shown above.
2) There is much more to the Fetch Api and to the Apis in general.
3) As you start working on more projects you will most probably start using things like async-await syntax for asynchronous programming and dealing with apis, sometimes you would be using popular libraries like axios to make requests, use tool like postman to test some api or use it while developing your own api, etc. Often while developing something with api you will come across terms like Rest Api, Api protocols, etc. **In short you don't need to know all of this just yet**. As you build more stuff you will become aware about this but for now you just need to know that such things exist.
 
