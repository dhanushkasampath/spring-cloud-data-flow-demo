How to perform stream processing using spring-cloud-data-flow


WHAT IS SPRING CLOUD DATA FLOW
==============================

It is a toolkit to build Microservice based Streaming and Batch data processing pipelines.

The data pipelines consist of Spring Boot Apps, Build using the Spring Cloud Stream or Spring Cloud Task microservice frameworks

WHEN TO CHOOSE SPRING CLOUD TASK OR SPRING CLOUD STREAM
======================================================

If your application is long lived, go for Spring Cloud Stream based microservices.
If your application is short lived, go for Spring Cloud Task based microservices.


source publish the event
processor process the event
Sink can consume that event

all these 3 can connect to each other using cloud stream.

We have used apache kafka as the messaging channel(kafka topic).

we will register above 3 microservices in spring cloud data flow, And then will create a one stream to verify how this microservice based streaming works in Spring Cloud Data flow.
Then all these 3 micro-services can talk to each other through that stream.

EXAMPLE
======

we are going to create 3 micro-services with having below dependencies in all 3

lombok
cloud stream
spring for apache kafka

1. product-service (source)
2. discount-service (processor)
3. courier-service (sink)


@EnableBinding has been removed by spring boot 3.x.x
@EnableBinding should be replaced by Supplier in Functional Programming


There is a jar file we need to run as "spring-cloud-dataflow-server"
we need to download that

Below is the url of spring cloud dataflow server dashboard
localhost:9393/dashboard

Also there is another jar to be downloaded as "spring-cloud-dataflow-shell"
