# serverless-javascript v2 based on Stealify - REiDEEN Release
The Overall Architecture or how we builded the fastest serverless production framework in the world.

## Ingreedents
Graal Compiler
Truffle Framework as absraction over ECMAScript2020
Couchbase Java 3.0 SDK DCP-Client
vertx JavaScript Bindings.

# serverless-javascript v1 
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

# Importent Notes about NodeJS MPM
1. Cluster listining in master can lead to better cpu util
2. Cluster listining in woker should be more performant but needs OS Level tuning
3. ker THs are only usefull when you can use shared memory with master. Scales better for less util functions.

Good thing is 1. 2. need no code change only the method changes from cluster fork to new worker
