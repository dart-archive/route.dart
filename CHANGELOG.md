# v0.5.0

## Breaking changes

- `UrlMatcher.urlParameterNames` has been changed from a method to a getter. The client code must be
   updated accordingly:

   Before:

        var names = urlMatcher.urlParameterNames();

   After:

        var names = urlMatcher.urlParameterNames;
