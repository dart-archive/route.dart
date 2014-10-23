# v0.6.0

## Features

- Introduced `reload({startingFrom})` method which allows to force reload currently active routes.
- UrlPattern now support paramerter values that contain slashes (`/foo/:bar*` which will fully match `/foo/bar/baz`)

BREAKING CHANGE:
The router no longer requires prefixing query param names with route name.
By default all query param changes will trigger route reload, but you can provide
a list of param patterns (via watchQueryParameters named param on addRoute) which
will be used to match (prefix match) param names that trigger route reloading. 
A short-hand for "I don't care about any parameters, never reload" is
`watchQueryParameters: []`.


# v0.5.0

## Breaking changes

- `UrlMatcher.urlParameterNames` has been changed from a method to a getter. The client code must be
   updated accordingly:

   Before:

        var names = urlMatcher.urlParameterNames();

   After:

        var names = urlMatcher.urlParameterNames;
