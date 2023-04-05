# kafka-basics-py
A basic consumer and producer python program for Confluent Kafka


## About *confluent-kafka*
**confluent-kafka-python** provides a high-level Producer, Consumer and AdminClient compatible with all
[Apache Kafka<sup>TM<sup>](http://kafka.apache.org/) brokers >= v0.8, [Confluent Cloud](https://www.confluent.io/confluent-cloud/)
and [Confluent Platform](https://www.confluent.io/product/compare/). The client is:

- **Reliable** - It's a wrapper around [librdkafka](https://github.com/edenhill/librdkafka) (provided automatically via binary wheels) which is widely deployed in a diverse set of production scenarios. It's tested using [the same set of system tests](https://github.com/confluentinc/confluent-kafka-python/tree/master/src/confluent_kafka/kafkatest) as the Java client [and more](https://github.com/confluentinc/confluent-kafka-python/tree/master/tests). It's supported by [Confluent](https://confluent.io).

- **Performant** - Performance is a key design consideration. Maximum throughput is on par with the Java client for larger message sizes (where the overhead of the Python interpreter has less impact). Latency is on par with the Java client.

- **Future proof** - Confluent, founded by the
creators of Kafka, is building a [streaming platform](https://www.confluent.io/product/compare/)
with Apache Kafka at its core. It's high priority for us that client features keep
pace with core Apache Kafka and components of the [Confluent Platform](https://www.confluent.io/product/compare/).



## Usage

- Clone the repository. Navigate to the the repository and install the required dependencies using
```bash
pip install -r requirements.txt
```

- Duplicate the ```getting_started.example.ini``` and rename it to ```getting_started.ini```

- Replace the placeholders with your respective credentials from Confluent Console.

- In the file ```consumer.py```, change the variable ```topic``` to your custom topic that you want to read from. Same with the ```producer.py``` file.

- Make the python files executable using 
```bash
chmod u+x consumer.py
chmod u+x producer.py
```

- Run the producer file using 
```bash
./producer.py getting_started.ini
```
- Run the consumer file using 
```bash
./consumer.py getting_started.ini
```

The messages should be printed out in the console and the ```consumer.py``` will wait for any new incoming messages.
Quit the ```consumer.py``` using Control+C.

## Contributing

Contributions are always welcome! If you have any improvements or new examples to add, please submit a pull request.

## License

This repository is licensed under the MIT license. See the [LICENSE](LICENSE) file for details.
