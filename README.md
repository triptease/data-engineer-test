# Data Engineer Test
### Back story

Triptease's data pipeline receives hundreds of events per second from tens of thousands of websites. One section of the pipeline is responsible for analysing and aggregating this raw data into metrics, which can be accessed quickly and efficiently from our client dashboard. We'd like you to replicate this part of the pipeline.

### The exercise

We have attached a sample containing three days' worth of 'page view' event data. We'd like you to create a service that ingests this data, performs some aggregations, and stores the output in a format which could then be served over an API. (We don’t expect you to write the API!)

Keep in mind that this service may have to scale to terabytes of data. We’d want the API to be able to provide the following:

* Count of page views per hour.
* Number of page views received in a given time period for a given account\_id.
* Number of sessions started per hour.
* Number of unique users per hour.

The events provided are not grouped by session, and these will need to be calculated by your pipeline. The rules defining a session are that:

* A session is a grouping of events with the same user\_id and account\_id
* Session expiry time is two hours, i.e. a new session will start if it has been 2 hours or more since the previous event.
* Sessions restart at midnight (so you do not have to calculate sessions across days)

You can return your solution as a zip file or upload it to GitHub. You should provide a readme file explaining your solution and any assumptions that were made during the exercise.