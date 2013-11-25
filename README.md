Braque-Swaggerjs
================

Builds a braque route file from a swagger.js resource.

Braque-Swagger is a simple helper package that will take a Swagger resource URL
and create a local api route file. This provides the ability to extra an entire
API for local use in a module. It provides rapid reference, and can be used to
write local tests for an API.

    ``` npm install braque-swagger ```

### Usage


### CLI
From the command line a route file can be created using the following

Arguments:
* url - Full Resource URL.
* file - Optional output file. Will dump to console when not provided

``` braque-swagger --url http://api.staging.formagg.io --file api.json ````
