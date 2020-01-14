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

  BROWSER -> sreedhar.com: Hey sreedhar.com! acreddy.com wants his address to be shared with just requests originated from acreddy.com. So sorry I cant share this information with you

  Basically this is CORS. The browser checks the **Access-Control-Allow-Origin** header and decides whether to give this response or not.

#### 04/12/2019

- ##### Hashing

  <span style="color:orange;"> Why cant hashing functions be one to one rather than many to one?<span>

  Because when a user password is hashed and stored then there is a chance of collision with other password.

- ##### Lazy Initialization in haskell

  Haskell has Lazy initialization.

  So what is lazy initialization?

  A function is evaluated only when the result of the function is used.

  Example:

  ```haskell
      take 24 [13,26..]
  ```

  In haskel take functions extracts first 24 elements from a list. And `[13,26..65]` in haskell returns `[13, 26, 39, 42, 65]` and this is an example of range.

  > Remember `[1,2,3]` is also a function in haskell.

  So if the last number is not provided `[13, 26..]` becomes a list of infinity numbers. But thats not how haskell evaluates the list. It sees what you want in `take 24 [13,26..]` and just evaluates the first 24 elements instead of the entire list.

#### 03/01/2019

- ##### Fast and maintainable patterns for fetching from a database - Sophiebits
  https://sophiebits.com/2020/01/01/fast-maintainable-db-patterns.html.
  I always wanted to know where parellel computation is useful and where FP solves the issues in it. In this blog its clear.
- Prototyping in JS : https://dev.to/lydiahallie/javascript-visualized-prototypal-inheritance-47co

#### 08/01/2019

- STORY. How can you scale your applications with K8s?

  https://www.youtube.com/watch?v=hZyUOvP7qv0

  [@19:14](https://youtu.be/hZyUOvP7qv0?t=1155) One of the best comments. :-) [my_view_on_sdojojfd_names](https://github.com/a-c-sreedhar-reddy/Learnings#27112019)

#### 09/01/2019

- A [blog](https://www.cio.com/article/3201193/7-reasons-to-switch-to-microservices-and-5-reasons-you-might-not-succeed.html) on Microservices.

  - Reduce downtime like if you want to fix a problem just pull that down and push the new one. Here queues will be helpful like until the service is up all the calls will be stored in the queue and service reads calls from the queue.

  - You can scale just a service rathar than the whole application.

  - Different stacks for different use cases.

- Trying to achieve [this](https://youtu.be/dZ-nMjka3l0?t=159) Donald Knuth.

#### 12/01/2020

- [Edsger W. Dijkstra - Lecture: Reasoning About Programs](https://www.youtube.com/watch?v=GX3URhx6i2E)

  - [game](https://youtu.be/GX3URhx6i2E?t=493) try to solve it. Go to the next point only if you had tried to solve the puzzle.
  - You would get adrenalin rush at [this](https://youtu.be/GX3URhx6i2E?t=1288). But to get that you should first try to solve the problem and experience the adrenalin rush.
  - Request by Dijkstra

    Having seen how we can convince ourselves that programs indeed are totally correct, please realise that if you have written a program and its not correct that is a little bit cowardly to say that your program had a bug. To call errors bug is a very primitive animistic attitude suggested that the bug has life of itself and that you are not totally responsible for it. The mean little bug crept in behind your back at the moment you were not looking yeah. Oh this is not true. If the program is not correct you made an error and my request my prayer so to speak is that you stop using the term bugs for program errors but call them what they are, ERRORS. Unless we change our language and call an Error an Error programming and computing science have not yet matured .
