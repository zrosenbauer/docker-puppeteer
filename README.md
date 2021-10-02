# docker-puppeteer    

Docker container with Chromium, node.js, and [puppeteer](https://github.com/puppeteer/puppeteer).

**NOTE:** Check the [Dockerfile](./Dockerfile) to see the current node version.

## Usage

`docker pull bluenovaio/docker-puppeteer:v1.0.0`

## Example Use

This can be used to run puppeteer in Docker, usually used when snapshotting create-react-app applications.

```dockerfile
FROM bluenova/docker-puppeteer:v1.0.0

RUN yarn
RUN yarn build

# Run a snapshoot tool i.e. react-snap
RUN yarn snapshot

# Expose port and run server
EXPOSE 8080
CMD [ "node", "./server.js" ]
```
