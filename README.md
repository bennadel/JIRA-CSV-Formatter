
# JIRA CSV Formatter

by [Ben Nadel][bennadel] (on [Google+][googleplus])

This is a super simple utility page that can take CSV text content, or a CSV 
file, and output the markup that JIRA can use to generate an HTML table in the 
issue comments. 

Run the JIRA CSV Formatter application.

All the CSV parsing is done on the client - no server required. And, the 
parser will try to calculate the most appropriate field delimiter based on 
how frequently commas, tabs, and colons appear in the input data. There's also
a checkbox to denote whether or not the data includes a header row. If it does
not (include a header row), column headers will be automatically generated 
using the A-Z alphabet.


[bennadel]: http://www.bennadel.com
[googleplus]: https://plus.google.com/108976367067760160494?rel=author
[invisionapp]: http://www.invisionapp.com/?source=bennadel.com
