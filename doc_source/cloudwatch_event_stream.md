# Amazon ECS Event Stream for CloudWatch Events<a name="cloudwatch_event_stream"></a>

You can use Amazon ECS event stream for CloudWatch Events to receive near real\-time notifications regarding the current state of your Amazon ECS clusters\. If your tasks are using the Fargate launch type, you can see the state of your tasks\. If your tasks are using the EC2 launch type, you can see the state of both the container instances and the current state of all tasks running on those container instances\.

Using CloudWatch Events, you can build custom schedulers on top of Amazon ECS that are responsible for orchestrating tasks across clusters, and to monitor the state of clusters in near\-real time\. You can eliminate scheduling and monitoring code that continuously polls the Amazon ECS service for status changes, and instead handle Amazon ECS state changes asynchronously using any CloudWatch Events target, such as AWS Lambda, Amazon Simple Queue Service, Amazon Simple Notification Service, and Amazon Kinesis Data Streams\.

An Amazon ECS event stream ensures that every event delivered at least one time\. If duplicate events are sent, the event provides enough information to identify duplicates\. For more information, see [Handling Events](ecs_cwet_handling.md)\.

Events are relatively ordered, so that you can easily tell when an event occurred in relation to other events\.

**Topics**
+ [Amazon ECS Events](ecs_cwe_events.md)
+ [Handling Events](ecs_cwet_handling.md)