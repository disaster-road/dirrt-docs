# DIRRT Docs
Developer Documentation for DIRRT, a class project for MIS 374

## Table of Contents <a name="table-of-contents">
- [Table of Contents ](#table-of-contents-)
  - [Introduction ](#introduction)
  - [Getting Started ](#getting-started)
  - [Understanding Bindings](#bindings)
  - [Incorporating JavaScript](#incorporating-js)
  - [External Data Sources](#external-data-sources)
  - [Additional Resources](#additional-resources)
  - [Important Contacts](#important-contacts)

## Introduction <a name="introduction"></a>
Welcome to the DIRRT Documentation! This guide serves as your compass 
through the features and functionalities of DIRRT, a web application 
developed using Budibase. Whether you're a developer, administrator, or 
end user, this documentation provides a roadmap to navigate the 
intricacies of DIRRT, helping you gain a full understanding of its 
functionality.

## Getting Started <a name="getting-started"></a>
This platform was created using [Budibase](https://budibase.com/), an 
online low-code platform. So, in order to get started, one will need 
access to the app developed through the platform. If you have not been 
granted access to the app, please email 
[rebekahcabral@utexas.edu](mailto:rebekahcabral@utexas.edu?subject=DIRRT&nbsp;Budibase&nbsp;), 
[irtorres@utexas.edu](mailto:irtorres@utexas.edu?subject=DIRRT&nbsp;Budibase&nbsp;), 
or 
[sara.hashim@utexas.edu](mailto:sara.hashim@utexas.edu?subject=DIRRT&nbsp;Budibase&nbsp;) 
to receive access.

## Understanding Bindings <a name="bindings"></a>
Budibases's binding system lies at its core. Binding allows you to pass 
data to variables, allowing  webpages to dynamically display data. You can 
find official Budibase documentation on these 
[here](https://docs.budibase.com/docs/introduction-to-bindings). Budibase 
uses its own syntax for working with bindings. This syntax is common to a 
popular JavaScript library called handlebar.js, which is used to 
dynamically populate HTML pages as they are rendered on the server. You 
can learn about this syntax by reading the official handlebar.js 
documentation [here](https://handlebarsjs.com/). In DIRRT, the most common 
use of these bindings involves retrieving the primary key of a 
table through the URL. This is done through Budibase's [URL 
params](https://docs.budibase.com/docs/url-parameters) system. 

## Incorporating JavaScript <a name="incorporating-js"></a>
Another feature of Budibase is its ability to incorporate JavaScript to 
achieve more custom behavior. An excellent overview of basic JavaScript 
can be found [here](https://www.w3schools.com/js/). JavaScript can be used 
to [transform](https://docs.budibase.com/docs/transformers) data from SQL 
queries and extract relevant data. JavaScript can also be used to perform 
data aggregations like `GROUP BY` in SQL by looping over data in a 
provider. Notably, the majority of the time--at least in my 
experience--SQL queries can replace the need for JavaScript. JavaScript 
can also be handy when specifying 
[actions](https://docs.budibase.com/docs/actions) in Budibase. Here, a dev 
could create very custom behavior. The possibilities with JavaScript are 
endless, and we would recommend playing around with it on Budibase to 
understand its full range of capabilities.

## Regular Expression Validation <a name="regex-validation"></a>
For more custom input validation, such as zip code or email validation. 
It's encouraged to incorporate [regular 
expressions](https://www.regular-expressions.info/#:~:text=A%20regular%20expression%20(regex%20or,files%20in%20a%20file%20manager.)), 
commonly referred to as regex. Regex is essentially a way to express a 
pattern in text. For instance, the `^` character represents the *start* of 
the text, a `$` represents the end of the text and a `\d` character represents a 
digit. So, the regex `^\d$` would match something like `6` or `8`, but not 
`74` or `spaghetti`. Atlassian--the company behind Trello--has some good 
examples 
[here](https://confluence.atlassian.com/proforma/regex-validation-1087521274.html) 
for advanced regex patterns. Notably, however, the majority of advanced 
regex patterns, especially the ones used for input validation, can be 
found on Stack Overflow with a quick search. 

## External Data Sources <a name="external-data-sources"></a>
DIRRT stores data inside of a MySQL database which Budibase queries to 
populate pages with relevant data. Budibase allows devs to write [custom 
SQL queries](https://docs.budibase.com/docs/mysql-mariadb) to fetch data. 
This can be used as a way to circumvent some of Budibase's more 
restrictive filtering features in its data providers, specifically when it 
comes to joining tables. 

When implementing some more advanced features like reporting, it might be 
useful to develop a [REST 
API](https://www.ibm.com/topics/rest-apis#:~:text=the%20next%20step-,What%20is%20a%20REST%20API%3F,representational%20state%20transfer%20architectural%20style.). 
Hypothetically, one could create a button or a CRON job to hit an 
endpoint, query for relevant data, and email users within a certain role 
outside of Budibase. Developing this within the confines of one 
semester--assuming the reader is a student--is probably infeasible, but 
it's a possible solution one could find outside of Budibase's features.

## Additional Resources <a name="additional-resources"></a>
- [Official Budibase 
Documentation](https://docs.budibase.com/docs/what-is-budibase)
- [Budibase 
University](https://www.youtube.com/watch?v=I2xvZPIv4IQ&list=PLEel-MMkFaJltK_jpKouKTCRht49FflKO)
- [SQL Overview](https://www.w3schools.com/mysql/mysql_sql.asp)
- [REST API Example](https://github.com/sundowndev/express-api-example)
- [Can't Stop Excel-ing](https://www.youtube.com/watch?v=YYl-EbgDHhg)

## Important Contacts <a name="important-contacts"></a>
- Chad Detwiler, chad@disasterroad.org
- Michael (Mike) Johnson, insitemotion@gmail.com
- Caleb Briggs, caleb.briggs@gmail.com
