# Data Engineer Test
### Back story
Triptease receives hundreads of events per second from tens of thousands of sites. One of the parts of pipeline is to analyze and aggregate this raw data into metrics so that they can be accessed from our client dashboard quickly and effiecntly. We'd like to you replicate this part of the pipeline.

### The excerise
In the data folder we have attached a sample of 3 days of our page view event data. We would like you take this data, and write a pipeline that ingests the files and inserters aggregate data into a database of your choosing which would then be served by an API (writing API not excepted). You can use any language or tool to assist you however we are looking for a repeatable solution such as batching with luigi or a streaming solution.

The example events do not including grouping events by session and this will need to be calculated by your pipeline. The rules defining a session are that:

* Sessions restart at midnight
* A session is a grouping of events with the same user\_id and account\_id with a less then 2 hour gap between them


Aggregates excepted:

* Per hour
* Per account id
* Session starts
* Page views

If you can return your solution as a zip or uploaded to github, it should contain a readme explaining your solution and any assumptions made during the excerise.

