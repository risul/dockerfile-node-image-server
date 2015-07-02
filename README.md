# [Dockerfile](https://registry.hub.docker.com/u/risul/node-image-server/) for NodeJS Image server

Installs the [Image-Resizer](https://github.com/jimmynicol/image-resizer) server with all dependencies.
This docker image is based on the [libvips](https://registry.hub.docker.com/u/marcbachmann/libvips/) image created by [Marc Bachmann](https://hub.docker.com/u/marcbachmann/).


## Supported tags

- [`latest`](https://github.com/risul/dockerfile-node-image-server/blob/master/Dockerfile)


## How to use

Run it using:

```bash
$ docker run -d -p 8090:8080 \
	--name=<YOUR CONTAINER NAME> \
	-e AWS_ACCESS_KEY_ID=<INSERT HERE> \
	-e AWS_SECRET_ACCESS_KEY=<INSERT HERE> \
	-e AWS_REGION=<INSERT HERE> \
	-e S3_BUCKET=<INSERT HERE> \
	-e TWITTER_CONSUMER_KEY=<INSERT HERE> \
	-e TWITTER_CONSUMER_SECRET=<INSERT HERE> \
	-e TWITTER_ACCESS_TOKEN=<INSERT HERE> \
	-e TWITTER_ACCESS_TOKEN_SECRET=<INSERT HERE> \
	-e SOCIAL_IMAGE_EXPIRY=86400 \
	-e IMAGE_EXPIRY=2592000 \
	-e IMAGE_EXPIRY_SHORT=86400 \
	-e JSON_EXPIRY=2592000 \
	risul/node-image-server:latest
```¨

More [info](https://github.com/jimmynicol/image-resizer#environment-variables) about the environment variables


## License

Licensed under [MIT](http://opensource.org/licenses/mit-license.html)