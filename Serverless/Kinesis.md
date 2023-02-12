# Kinesis

Kinesis is a scalable streaming service within AWS designed to ingest large quantities of data and allow consumers access to that data.

For that reason, Kinesis is ideal for dashboards and large scale real-time analytic needs.

## Kinesis Data Firehose

Kinesis Date Firehose is a fully managed service to load data for data lakes, data stores, and analytics services.

It offers automatic scaling, and is fully serverless.

It isn’t a real-time product, but it offers near real-time delivery (~60 seconds).

Delivery is performed after either 60 seconds pass, or the buffered data being received hits 1MB in size.

Firehose supports transformation of data on the fly via Lambda.

Firehose is pay-as-you-go with billing based on the amount of data passing through the service.

## Kinesis Data Analytics

Kinesis Data Analytics is a real-time data processing product.

Experts say it’s an easy way to analyze streaming data, gain actionable insights, and respond to your business and customer needs in real-time.

Kinesis Data Analytics ingests data from Kinesis Data Streams or Firehose and can then process the data it receives using SQL.

## Kinesis Video Streams

Used to ingest live video data from producers such as security cameras, smartphones, cars, drones, etc.

Kinesis Video Streams automatically provisions and elastically scales all of the infrastructure needed to ingest streaming video data from millions of devices.

Kinesis Video Streams can persist and encrypt data.

Data inside of Kinesis Video Streams can be accessed only via APIs, not directly via storage.
