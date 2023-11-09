# News Demo go app

All credits to @freshman [starter files](https://github.com/Freshman-tech/news-demo-starter-files)

Tutorial:
https://freshman.tech/web-development-with-go/

![demo](https://ik.imagekit.io/freshman/news-demo_MrYio9GKlzSi.png)

What was changed:
- `X-Api-Key` in request header instead of query
- input maxlength as per API specs
- Dockerfile.dev for air live reload
- Dockerfile for deploying to [fly.io](https://fly.io)

TODO - refactor noodles into several files

## Prerequisites

You need to have [Go](https://golang.org/dl/) installed on your computer. Or you may use docker and docker compose for dev purpose


## Get started

- Clone or download this repository to your filesystem.

```sh
$ git clone https://github.com/samvimes01/news-api-go-app
$ cd news-api-go-app
$ docker compose up
```

- Deploy is possible to [fly.io](https://fly.io). It automativally detects Dockerfile. Without it assets aren't deployed and app fails
```sh
$ fly auth login
$ flyctl launch // No for deploy since there are env secrets
$ fly secrets set NEWS_API_KEY=blah // het your key at newsapi.org; secrets are available ar runtime as env vars
$ flyctl deploy
```
