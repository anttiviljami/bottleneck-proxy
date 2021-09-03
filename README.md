# bottleneck-proxy

[![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/anttiviljami/bottleneck-proxy/blob/master/LICENSE)
[![Dependencies](https://david-dm.org/anttiviljami/bottleneck-proxy.svg)](https://david-dm.org/anttiviljami/bottleneck-proxy)
[![npm version](https://img.shields.io/npm/v/bottleneck-proxy.svg)](https://www.npmjs.com/package/bottleneck-proxy)
[![Buy me a coffee](https://img.shields.io/badge/donate-buy%20me%20a%20coffee-orange)](https://buymeacoff.ee/anttiviljami)

Reverse proxy to limit concurrent HTTP requests to a target endpoint

Built to deal with backends that don't fully support concurrent requests such as
running AWS SAM `sam local start-api --warm-containers EAGER`

## Quick Start

```
npx bottleneck-proxy http://localhost:3000
# proxy listening at http://0.0.0.0:5000
# forwarding to http://localhost:3000 at max 1 concurrent request
```

## Usage

```
bottleneck-proxy - Reverse proxy to limit concurrent HTTP requests to a target endpoint

  USAGE

      $ bottleneck-proxy --help
      $ bottleneck-proxy --version
      $ bottleneck-proxy [-c max_concurrency] [target_url]

      By default, bottleneck-proxy will listen on 0.0.0.0:5000 and set max
      concurrency to 1.

  OPTIONS

      --help             Shows this help message

      -v, --version      Displays the current version of bottleneck-proxy

      -d, --debug        Show debugging information

      -c, --concurrency  Max number of concurrent requests (default: 1)

      -p, --port         Port to listen on (default: 5000)

      -h, --host         Host to bind to (default: 0.0.0.0)

```

