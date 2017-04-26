# aws-tools

# Prerequistes

 * bash
 * aws-cli
 * Properly configured AWS credential for AWS Command Line Interfaces.
 
# sqs

Dump (and delete) messages from AWS SQS queue as JSON into STDOUT.

## Install

```bash
$ curl https://raw.githubusercontent.com/t-nasu/aws-tools/master/sqs > /path/to/bin/sqs
```

## Usage

```
$ sqs --help
Usage: sqs [OPTIONS] command
  This script dump or import messages from/to AWS SQS queue.

Example (Migrate messages from dql to normal queue) :
   sqs dump --u https://sqs.ap-northeast-1.amazonaws.com/xxxxxxxxx/foo_dlq | sqs import --u https://sqs.ap-northeast-1.amazonaws.com/xxxxxxxxx/foo

Command:
   dump    receive messages and output to stdout, then delete these messages.
   import  send messages to queue from stdin

Options:
  -h, --help
      --version
  -n, --max_number_of_messages [num] (1-10, Default: 10)
  -u, --queue-url [url]
  ```
