
# JIRA CSV Formatter

by [Ben Nadel][bennadel] (on [Google+][googleplus])

This is a super simple utility page that can take CSV text content, or a CSV 
file, and output the markup that JIRA can use to generate an HTML table in the 
issue comments. 

**[Run the JIRA CSV Formatter application](http://bennadel.github.io/JIRA-CSV-Formatter/)**.

So, for example, if you were to paste in the CSV data:

```txt
ID,Sales Associate||Name,Date Hired,Total Sales,December,November,October,September,August
1,"Kim Smith","Feb 1, 2015",28,4,4,1,9,10
2,"Joanna Ho","Jul 4, 2015",21,5,3,9,0,4
3,"Tricia Clark","Mar 27, 2015",37,7,6,7,2,15
4,"Anna Banana","Feb 2, 2015",10,3,1,1,1,4
5,"Lisa Masters","Jun 19, 2015",3,0,0,0,1,2
```

... it would output the following JIRA markup:

```txt
||ID||Sales Associate\|\|Name||Date Hired||Total Sales||December||November||October||September||August||
|1|Kim Smith|Feb 1, 2015|28|4|4|1|9|10|
|2|Joanna Ho|Jul 4, 2015|21|5|3|9|0|4|
|3|Tricia Clark|Mar 27, 2015|37|7|6|7|2|15|
|4|Anna Banana|Feb 2, 2015|10|3|1|1|1|4|
|5|Lisa Masters|Jun 19, 2015|3|0|0|0|1|2|
```

As you can see, it uses the double-pipe to delineate the header row values and
the single-pipe to delineate the body row values.

All the CSV parsing is done on the client - no server required. And, the 
parser will try to calculate the most appropriate field delimiter based on 
how frequently commas, tabs, and colons appear in the input data. There's also
a checkbox to denote whether or not the data includes a header row. If it does
not (include a header row), column headers will be automatically generated 
using the A-Z alphabet.


[bennadel]: http://www.bennadel.com
[googleplus]: https://plus.google.com/108976367067760160494?rel=author
[invisionapp]: http://www.invisionapp.com/?source=bennadel.com
