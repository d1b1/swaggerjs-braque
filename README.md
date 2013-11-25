Braque-Swaggerjs
================

Builds a braque route file from a swagger.js resource.

Braque-Swagger is a simple helper package that will take a Swagger resource URL
and create a local api route file. This provides the ability to extra an entire
API for local use in a module. It provides rapid reference, and can be used to
write local tests for an API.

``` npm install braque-swagger ```

### CLI Options
From the command line a route file can be created using the following

Arguments:
* --url (or -u) : Full Resource URL.
* --file (or -f) : Optional output file. Will dump to console when not provided

``` braque-swagger --url http://api.staging.formagg.io --file api.json ````

### Workflows
There are a number of possible workflows for braque and swaggerjs-braque. 

*** Local API development ***
During the development of an API, the swaggerjs-braque code can be used
to dump a swagger.js api-docs resource into a braque formatted file. Using
braque and mocha, a developer can write tests in the same pattern needed 
for an external implimentation; authentication etc.

*** Implementation ***
During the development of a site or project that impliments all or part of an API,
use this CLI command to regenerate a local route file. Since the route file is tracked
in git, changes to the API, such as new, deleted or altered endpoints will be
are easier to manage.


### Background
This code is designed to work with [braque](https://npmjs.org/package/braque) which provides
an light weight pattern for abstracting a rest API into a node.js codebase. It removes the
need to include API specific implementions.

The `braque` project grew out of need to limit the number of dependencies for an express app that uses
a number of external APIs to provides site features; github, twitter, facebook, flickr and foursquare.
Every API implemnetion in npm seems to follow different patterns. Braque uses api route file (json) to
construct an internal code api for each external API.
