# Introduction to messaging

* When we start deploying multiple applications, they will need to communicate with one another
* There are two patterns of application communication
  * Synchronous communications
  * Asynchronous/Event based (with a queue)
* Synchronous between application can be problematic if there are sudden spikes of traffic
* What if you need to suddenly encode 1000 videos but usually it's 10?
* In that case, it's better to decouple your apps
  * SQS: queue model
  * SNS: pub/sub model
  * Kinesis: real-time streaming model
* These services can scale independently from our apps
