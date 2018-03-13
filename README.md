# REST API using RabbitMQ
### Kyeongsoo Kim, March 2018

## Introduction
 Simple RESTful message queuing app using NodeJS and RabbitMQ.
 When messages are sent with keys, app creates to an exclusive queue, binds it to an direct exchange "hw3" with all provided keys.

 > The routing algorithm behind a direct exchange is simple - a message goes to the queues whose binding key exactly matches the routing key of the message. - from RabbitMQ website


## REST API 
It consists of two end points.

 <pre>
/listen { keys: [array] }

waits to receive a message and returns it as { msg: }
</pre>

<pre>
/speak { key:, msg: }
Publishes the message to a direct exchange with provided key
</pre>

