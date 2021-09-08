# docker-php-mongodb

## Docker command cheat sheet

* `docker build -t example-name:tag .`

## How to use this image?

```bash
docker run --rm --interactive --tty \
--volume $PWD:/app \
example-name:tag dump
```