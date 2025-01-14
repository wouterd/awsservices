# Amazon Web Services (AWS) (version 1.3)

This module provides actions and UI to leverage services on the Amazon Web Services (AWS).

The following services are facilitated using this module:

- S3 - Simple Storage Service
  - Explore buckets UI
  - Download, upload, delete and edit files
- SQS - Simple Queueing Service 
  - Explore queues through UI
  - Send and receive messages
  - Message attributes
  - Retrieval of queue attributes (e.g. depth) for monitoring purposes
  - Examples for high volume processing
- SNS - Simple Notification Service
  - Explore topics through UI
  - Publish messages to topics (incl message attributes)


The following flows of authentication are supported to access all of the above services:

- Static (Access/Secret)
- Cognito (USER_PASSWORD flow)



**Note**: The Amazon SQS and Amazon S3 module were merged into this module. Because of the high overlap of common functionality it became easier to maintain and extend into this single module.



## Dependencies

This module depends on the following modules:

- Encryption (to encrypt AWS credentials in the database)

- Library Logging (to redirect logging from the AWS libraries to Mendix lognodes)

  

## How to upgrade from earlier SQS/S3/xx modules

The earlier S3 and SQS modules were using a earlier version of the Amazon SDK. Therefore all AWS jars should be removed from the `userlib` directory.

**Important note**:  

Steps are:

- Remove all jars from the `userlib` directory which have a corresponding file ending with `AWSSQSConnector.RequiredLib` 
- Remove all jars from the `userlib` directory which have a corresponding file ending with `AWSS3Connector.RequiredLib` 

Both older modules should have a high overlap of found files.

## Contributors

Special thanks going to:

- Wouter Danes (@wouterd) for adding SNS and Cognito

