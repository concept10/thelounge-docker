# docker-lounge

Docker container for [The Lounge](https://thelounge.github.io/), a self-hosted web IRC client.

## Running a container

Using the example docker-compose.yml file
```sh
$ docker-compose up --detach
```

or

```
$ docker run --detach \
		--name lounge \
		--publish 9000:9000 \
		--volume ~/.lounge:/home/lounge/data \
		--restart always \
		thelounge/lounge:latest
```

## Environment variables

You can control how The Lounge is started through the following environment variables;

- `HOST` (equivalent to the `-H, --host` CLI option)
- `PORT` (equivalent to the `-P, --port` CLI option)
- `BIND` (equivalent to the `-B, --bind` CLI option)

## Where is data stored?

Lounge reads and stores its configuration, logs and other data at `/home/lounge/data`.
