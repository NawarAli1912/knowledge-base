- it's a way to see how the sql engine retrieve the data for optimization purposes.
- sql server engine will calculate some possible ways to retrieve the data and choose the best one but that's not necessarily will be the optimal one 
- here we can show a benefits of using view because it calculate the execution plan once and then use it when we call it.
- we can view the execution plan in different ways :
  1. SET SHOWPLAN_ALL ON; it will show it as a text tree;
  2. we can press the display execution plan button to show a graphical representation of it. we should also press the include actual execution plan, if not we will see the estimated one.
     the difference between them is that the estimated one is the one which generated before the engine run the query vice versa so the actual one will have the real run-time statistics.
  3. turn on live query statistics useful when we run a query that doesn't want to finish.