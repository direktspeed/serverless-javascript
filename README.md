# serverless-javascript
Serverless JavaScript

because i always repeated the server parts of my applications i need to source that out.

## Core Concepts
- Running a Worker Pool for functions that can get triggered by process stdin and produce stdout
- Running a Woker Pool that Pools and Processes Data.
- Running a Webserver that executes a function per url. in a worker and returns the response.
- support mpms multi processing models
- prefork - one process maintains workers that are already started sync
- workers - one process maintains workers that can handle many requests async
- event - similar to workers but if handling connections it would have a listner per worker


## Core Algos
- HealthChecking
- Connection Handling
  - stdin is a connection
  - grpc HTTPRequests
  - http2
  - netsocket fd

## Usage

## deno serverless-javascript

## NodeJS serverless-javascript


# Scenario 1
Listening on a eventbus for http requests process them create response

# Scenario 2
Listening on http2 and execute function by request url

