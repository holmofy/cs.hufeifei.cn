---
title: kafka
categories: kafka
keywords: kafka,命令行,参考手册
description: kafka官方命令行手册
---

## get started

参考: 
* https://docs.confluent.io/platform/current/kafka/post-deployment.html

### start kafka-broker
```bash
bin/kafka-server-start.sh -daemon config/server.properties
```

### start kafka-connect
```bash
bin/connect-standalone.sh -daemon \
    config/connect-standalone.properties \
    config/debezium-mysql.properties
```

### list topic
```bash
bin/kafka-topics.sh --zookeeper localhost:2181 \
    --list
# Use kafka-broker instead of zookeeper. Same below
bin/kafka-topics.sh --bootstrap-server <kafkahost:port> \
    --list
```

### desc topic
```bash
bin/kafka-topics.sh --bootstrap-server <kafkahost:port> \
    --topic $1 \
    --describe
```

### create topic
```bash
bin/kafka-topics.sh --bootstrap-server <kafkahost:port> \
    --topic $1 \
    --partitions $2 \
    --create
```

### remove topic
```bash
bin/kafka-topics.sh --bootstrap-server <kafkahost:port> \
    --topic $1 \
    --delete
```
### produce msg to topic
```bash
echo "msg" | bin/kafka-console-producer.sh \
    --bootstrap-server <kafkahost:port> \
    --topic $1
```

### consume msg from topic
```bash
bin/kafka-console-consumer.sh --bootstrap-server <kafkahost:port> \
    --topic $1 --from-beginning --property print.timestamp=true
```

### search msg from topic
```bash
bin/kafka-console-consumer.sh --bootstrap-server <kafkahost:port> \
    --topic $1 --from-beginning | grep $2
```

### describe consumer group
```bash
bin/kafka-consumer-groups.sh --bootstrap-server <kafkahost:port> \
    --group $1 \
    --describe
```

### reset consumer offset for topic
```bash
# preview
bin/kafka-consumer-groups --bootstrap-server <kafkahost:port> \
    --group <group_id> \
    --topic <topic_name> \
    --reset-offsets --to-earliest
# execute
bin/kafka-consumer-groups --bootstrap-server <kafkahost:port> \
    --group <group_id> \
    --topic <topic_name> \
    --reset-offsets \
    --to-earliest \
    --execute
```
other resetting options, run kafka-consumer-groups for details
* --shift-by <positive_or_negative_integer>
* --to-current
* --to-latest
* --to-offset <offset_integer>
* --to-datetime <datetime_string>
* --by-duration <duration_string>

### producer performance
```bash
bin/kafka-producer-perf-test.sh --bootstrap-server <kafkahost:port> \
    --topic <topic> \
    --num-records <msg-count> \
    --record-size <record-bytes> \
    --throughput <messages/sec> \
    --producer.config <producer-config-file>
```

### consumer performance
```bash
bin/kafka-consumer-perf-test.sh --bootstrap-server <kafkahost:port> \
    --topic <topic> \
    --messages <msg-count> \
    --group <gid:default:perf-consumer-49221> \
    --fetch-size <fetch-size:default:1048576> \
    --date-format <timestamp-format:default:yyyy-MM-dd HH:mm:ss:SSS> \
    --consumer.config <consumer-config-file> \
    --from-latest
```