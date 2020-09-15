- ## REDIS

* Remote Dictionary Server is an open source key-value data store
* It keeps information in memory rather than on the hard drive to speed up response times
* Memcached is a similar open source data store, but doesn't offer the same features
* Redis data types include strings, lists, sets, sorted sets, hashes, bitmaps, hyperloglogs
* Redis is good for caching with its low latency, chat/messaging with its variety of data structures, gaming leader boards with sorted sets, session storage with low latency and high scalability, media streaming with its ability to manifest files, geospacial tasks with data structures, Machine learning with its ability to process live data, and real time analytics by using it with Apache Kafka and Amazon Kinesi
* It works well with JavaScript, Node, and many other languages
* AWS can fully manage it

## Queue

* A data structure that handles elements in sequence like a stack
* Enqueue adds an item to the end of the line
* Dequeue takes an item away from the front of the line
* isEmpty() returns a boolean
* Top() returns the next in line
## Task Queue Overview

* One kind of queue handles tasks one at a time until finished
* Another kind has the ability to schedule tasks for a specific time in the future

# Task Queue - FIFO

* First in first out handles items in a queue in the order they were added, always doing the oldest item next
* Sometimes certain tasks have a higher priority and we would want those to skip to the front of the line
* Having three priority levels would let the highest priority items get handled first and the least priority messages sent when all others have been handled
* Sometimes it is good to reevaluate the queues, especially if one priority level tends to get more volume

# Bull

* Bull is a node library that uses a fast queue system with redi
* Bull can be installed with (npm install bull --save)
* It needs a redis server running and can be installed using Docker
* a queue is created with (const myFirstQueue = new Bull('my-first-queue'))
* A producer is a node program that adds jobs to a queue
* A consumer or worker is a node program that defines a process
* Listeners listen to events that happen in the queue
* Job life cycles are job added, wait/delayed, active, completed/failed, finished
* Jobs can be handled FIFO (default), LIFO, Delayed for an amount of time, Prioritized, Repeatable