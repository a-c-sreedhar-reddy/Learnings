# Learnings

What happens in a day?

#### 23/11/2019

- If it does not have a return keyword its not a function its procedure.

- When I was studying 9th class my math teacher taught me that in a function each element in a domain could be mapped to only one value in range. I could not understand why. But now the same thing is what I learn in FP. And the reason I feel is it makes debugging obvious. Else I would have to go into function and see which one will be returned.

- I love to get back my childhood brain. Because back then when I saw fogoh(x) it was beautiful and I owned it. But now I think from an external perpective.

- More than side effects etc FP is nothing but being obvious. When you look at the function you need to be like , OK this does this and this will be the output And currying and Partial application proves that. Because in currying the inner function uses the variable passed by the outer function. But its obvious that the value you get is immutable and hence constant.

#### 27/11/2019

- Equational Reasoning :

  ```javascript
  getPerson(function onPerson(person) {
    return renderPerson(person);
  });
  ```

  is same as

  ```javascript
    function getPerson(rederPerson);
  ```

  everyone might have done this but the only thing is we dont know names. And names are tough.
  So if you find some new names just read about it and you would be like either

  > I did this before just I dont know the name.

  or

  > YEAH now I get it why they named it in this way.

- https://www.youtube.com/watch?v=7XvgqDlp8sQ
  Interesting video about kubernetes. Kubernetes just groups all servers in a cluster and deploy containers.

#### 28/11/2019

- ##### CORS: Cross-Origin Resource Sharing
  So sreedhar.com needs a resource from acreddy.com

  sreedhar.com : Hey browser I need acreddy.com/address

  BROWSER -> sreedhar.com : OKAY wait till I get the request.

  BROWSER -> acreddy.com : Hey acreddy.com I need /address.

  acreddy.com -> BROWSER : Chennai. Here is my address but only give this to requests
                          which came from acreddy.com.

  BROWSER : Okay I got the address. But acreddy.com want it to be shared with requests originated from acreddy.com But here sreedhar.com is requesting the address. Okay I am not going to give this address to sreedhar.com

  BROWSER -> sreedhar.com: Hey sreedhar.com! acreddy.com wants his address to be shared with just requests originated from  acreddy.com. So sorry I cant share this information with you

  Basically this is CORS. The browser checks the **Access-Control-Allow-Origin** header and decides whether to give this response or not.
