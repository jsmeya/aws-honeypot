# aws-honeypot
EC2 instance in AWS paired with the [T-Pot](https://github.com/telekom-security/tpotce) framework.

---

## Background

The goal of this project was to gain relevant knowledge of the AWS platform and learn more about centralized, routine attack methods. The first part of the project was setting up everything, like deploying the EC2 instance and installing the T-Pot framework. The second part was a mix of upkeep and observation, and the third part was building a custom log parser in Python.

## Setup

Setup included launching an EC2 instance in AWS and installing the T-Pot framework. This first consisted of configuring a baseline for the instance, which included operating system, memory, storage, and some other attributes. Once launched, a PEM key was used to access the instance over SSH. From there, all that was left was to install T-Pot on the machine, which was a relatively smooth and straightforward process.

## Deployment

The plan was to run this over a seven-day period to observe attacker volume, methods, and patterns across different days of the week. This included weekends, since the honeypot was ran from a particular Sunday to the following Sunday. T-Pot offers a centralized view of attacker information from a Kibana dashboard, which displayed total attacks and geographical information. Germany was among the countries of the highest attacker volume. Moreover, a notable portion of attack sources were automated scanners or bots, which was interesting.

Total attacks/connections: `140,000+`

## Log Analysis

A log parser in Python is *actively* being built to personalize data aggregation. It's important to note that the cleanup of this data has been a heavy part of this project since all of T-Pot's data is from a variety of different sources with different formats. Nonetheless, by the end of it, some additional valuable insight should be obtained.
