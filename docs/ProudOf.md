# Interesting Problem

## One thing you’ve created that you are particularly proud of
## Example of an interesting technical problem I have solved

### Situation:
The development team moved their monolithic application into microservices. The development team decoupled their services into sub services but the solution was not optimal.

### Problem:
1. The application was making too many calls to the database. They used the database pretty much as a placeholder. The application sometimes used up all the concurrent connections allowed. This caused a bottleneck.
2. Their retry logic was embedded in the source code. When an upload fails, the retry loop and timeout is within the same code. With the loops and timeout, I felt like this was an inefficient solution. The services ends up busy being a lot.



### Solution:
My solution was to use message queues. Using a publisher and subscriber model, we don’t have to use the database as a placeholder.

I also suggested the implementation of step functions to do the retry logic.

### Example:
1. A teacher or trainee uploads their documents -videos and lesson plan 
2. The upload service drops the files into a bucket. (updates the db)
3. A cron service, on an interval, invokes the generate service to query the database, look for new files on the table and get the files from the bucket and send it to the 3rd party app (updates the db)
4. Another cron job, periodically ask the 3rd party app if it has finished processing the documents. 
5. If it has finished, it get the file or information from the 3rd party app and forwards it to the normalizing service.
6. The normalizing service updates the database.
7. The evaluator can now look at the normalized documents. 


#### My adapted proposal:
1. When the documents are added to the bucket a serverless function picks it up and puts it in a queue. 
2. The Transfer Service will pick from the queue and forward it to the 3rd party application.
3. If the transfer fails, the step function will retry.

#### Callback
1. Now the 3rd party app will callback our service once it has finished proofreading our documents and processing the user’s video. Instead of us ping the 3rd party application.
2. It has several more step functions and serverless function logic to make sure the returned files are correct.
3. And then it will be queued for normalization.

### Impact:
The impact of this was apparent. The workflow seems much more intuitive. Especially with the retry logic and not having to use the database as a placeholder.

### Lesson:
One lesson I have learned is that we should constantly find ways to improve our workflow with emerging technologies. The reason why this workflow was not adopted earlier was because the technology just wasn’t there. We should look beyond just using containers. We should always leverage better technology that would improve our workflow. 
