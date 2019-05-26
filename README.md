# Git Review

[![CircleCI](https://circleci.com/gh/USA-RedDragon/GitReview-caddy/tree/master.svg?style=svg)](https://circleci.com/gh/USA-RedDragon/GitReview-caddy/tree/master) [![Caddy](https://images.microbadger.com/badges/image/jamcswain/gitreview-caddy.svg)](https://microbadger.com/images/jamcswain/gitreview-caddy "Get your own image badge on microbadger.com")

## Deploying

The Docker images for the current master branch are found on [Docker Hub](https://hub.docker.com/u/jamcswain) under `gitreview-caddy`. Versioning will be implemented once we reach stable 1.0.

The below documentation will go through the information you need.

As far as best practices, and how to deploy containers, a Google search is your best friend.

## Environment Variables

| Environment Variable |                                   Details                                   |            Example            |
| -------------------- | --------------------------------------------------------------------------- | ----------------------------- |
| ACME_AGREE           | Agree to ACME TOS                                                           | true                          |
| URL                  | The URL the app is running on                                               | url.domain.com                |
| TLS_OPTIONS          | The TLS options for Caddy, off for local development, email for LetsEncrypt | email@domain.com              |
| API_HOST             | The hostname of the API                                                     | localhost                     |
| API_PORT             | The port of the API                                                         | 3000                          |
| CLIENT_HOST          | The hostname of the client                                                  | localhost                     |
| CLIENT_PORT          | The port of the client                                                      | 3001                          |
| BASIC_AUTH_OPTIONS   | Caddyfile basic auth options                                                | basicauth / username password |

## Volumes

|     Path     |                Details                |
| ------------ | ------------------------------------- |
| /root/.caddy | The persistent SSL certificate volume |
