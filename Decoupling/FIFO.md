# FIFO Queue

* FIFO = First In First Out (ordering of messages in the queue)
* Limited throughput: 300 messages/s without batching, 3000 messages/s with batching
* Exactly-once send capability (by removing duplicates)
* Messages are processed in order by the consumer
