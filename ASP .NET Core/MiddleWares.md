- they are set of function or pipeline that implement the Chain of Responsibility Design pattern
- the request should pass throw each one of those function to be processed and handled by the server 
- finally the server generate the http response and return it to the caller
- usually the last one is the one that is responsible of handling the logic and has it's own pipeline
- they are responsible for cross-catting concerns each request must go throw all of them 
- there is another pipeline which is specific for the request called 
  [[Filters]]

---
#dotnet