# Amazon MQ

* SQS, SNS are "cloud-native" services, and they are using proprietary protocols from AWS
* Traditional apps running from on-premise may use open protocols such as: MQTT, AMQP, STOMP, Openwire, WSS
* When migrating to the cloud, instead of re.engineering the application to use SQS and SNS, we can use Amazon MQ
* Amazon MQ = managed Apache ActiveMQ
* Amazon MQ doesn't scale as much as SQS/SNS
* Runs on a dedicated machine, can run in HA with failover
* Has both queue features (SQS) and topic features (SNS)
