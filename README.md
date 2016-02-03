# What is this?

This is a demonstration of an [issue described in a stackoverflow
question](http://stackoverflow.com/q/34065614/322152).

# The Challenge

Make this solution build in VS2015 i.e. within the IDE, using `Project > Build`.

The solution _can_ be built from the command line using:

```
msbuild /tv:12.0 /p:Platform="Any CPU" /p:Configuration=Debug
```

However, that's not the point.  We need to be able to build it in the IDE.

# What makes it fail?

There's a file, `RequiredToolsVersion.targets`, imported into
`toolsversion.csproj` that will trigger a build error if it's built with a
ToolsVersion other than 12.0.

# Really, why?

See the [question on stackoverflow](http://stackoverflow.com/q/34065614/322152).
