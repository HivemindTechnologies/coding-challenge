# Tweet ui

Sentiment analysis ui to check whether your tweet is ok or not.

## Format
The ui will query the sentiment analysis backend api using a POST to `$BASE_URL/api/analysis` containing the following json body:
```json
{"content":"This is a bad sentence"}
```

It expects a response in the format:
```json
{"toxicity":false,"threat":false,"sexualExplicit":false,"severeToxicity":false,"obscene":false,"insult":false,"identityAttack":false}
```

The `$BASE_URL` environment variable can be optionally set, otherwise will default to empty string.

## Usage

You can run the service locally by running 
```sh
npm install
npm run webpack:server
# or
BASE_URL=http://localhost:8080 npm run webpack:server
```

## Deployment

You can deploy the ui as a static website or as a service, it's up to you. 

### Static website
To bundle the ui for static website deployment, run
```sh
npm install
npm run webpack:bundle
# or
BASE_URL=http://localhost:8080 npm run webpack:bundle
```
This will bundle the html and js files into the `dist/` folder which you can then deploy.
To test that the site works, run 
```sh
npm run serve
```
and open `http://localhost:9000`

### Service
To deploy the ui as a service, you can use the provided [Dockerfile](./docker/Dockerfile) which runs the ui in an integrated http server, e.g. by running:

```sh
docker build -t="hivemind/tweet-ui" -f docker/Dockerfile .
docker run -ti -p 9000:9000 -e BASE_URL=http://localhost:8080 hivemind/tweet-ui:lates
```
