# docker-compose-mailserver

A mail server running Postfix and Dovecot. You should build the required images for [Postfix](https://github.com/bhorvath/docker-postfix) and [Dovecot](https://github.com/bhorvath/docker-dovecot) before continuing.

## Configuring

Copy `.env-example` to `.env` and edit the environment variables as required.
Variable      | Description
--------      | -----------
LISTEN_IP     | The IP address that will be bound to exposed ports
MAIL_DOMAIN   | The domain for which mail will be served
TLS_CERT_FILE | The path to the TLS certificate (this path must be accessible within the containers)
TLS_KEY_FILE  | The path to the TLS key (this path must be accessible within the containers)
TZ            | The timezone of the mail server

## Running

Start the containers like so:
```
cd docker-compose-mailserver
docker-compose -p mail up -d
