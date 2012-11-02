# Service Oriented Architecture at Square

Really interesting talk from Chris Hunt (Software Engineer at Square Inc.)

He gave us an understanding how Square services communicate with each other. It was also interesting to see how they handle some parts of security, mainly because they deal with huge amounts of money transactions.


### Slides

[http://chrishunt.co/talks/soa/](http://chrishunt.co/talks/soa/)

### Notes

- They user a fdoc ([https://github.com/square/fdoc](https://github.com/square/fdoc)) app to generate documentation
- It's a Documentation Oriented Development (really like this and this is something we've been trying to implement with surechem direct). It fails if not matching with doc
- fdoc generates a fdoc file with a lot of ??? that you fill after, so it's not entierly automated
- They use foreman to load fake servers where the tests run against. This is very useful to abstract the tests from the real server and data dependency
- We can use cane ([https://github.com/square/cane](https://github.com/square/cane)) "rake quality" to run tests based on our DEPs
- They use jetpack ([https://github.com/square/jetpack](https://github.com/square/jetpack)) to bundle everything together
- They user airbreak to handle errors exceptions
- They user cubism.js to build the graphs based on data metrics for payments, etc
- They use splunk to analyse logs and interact with logs (very nice!)
- They user Organization Unit from a SSL certificate to verify if you access a given part of the system

### Book

Growing Obj Oriented software, guided by tests

### Questions

Q: I noticed you guys don't use chef, any reason?<br/>
A: It's an internal problem with square just because they started with different tools and it's comlicated for them to switch now. The feedback that I had was "if we'd do it now we'd do it with chef. Chef kicks ass :)"