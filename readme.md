HTTP(s) -> SQS Queue
####################

[![Join the chat at https://gitter.im/markgandolfo/http-to-sqs](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/markgandolfo/http-to-sqs?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

A simple golang service that will accept a http request at a specific url, and send the params to an sqs queue.

There will be configuration via a config file (perhaps yaml), for example:

    ---
    project_name:
      path: /api/v1/create_article
      sqs: create_article

Another config file will be checked for aws credentials, if it's not present, a check in the ENV for `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`

#### Suggested phase 2

* HTTP/HTTPS support
* HTTP Basic Auth support
