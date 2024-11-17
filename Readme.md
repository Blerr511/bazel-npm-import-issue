# Bazel Fails to Fetch fast-deep-equal Due to HTTP 304 Not Modified Error

I'm encountering an issue where Bazel fails to fetch the fast-deep-equal@3.1.3 package when using the npm_translate_lock rule from Aspect's rules_js. The build process halts with an error indicating that a GET request returned a 304 Not Modified status code, which Bazel does not handle properly.

This issue seems specific to the fast-deep-equal package, as other packages are fetched without any problems.

To reproduce the issue try to run

```shell
bazel run //:start
```
