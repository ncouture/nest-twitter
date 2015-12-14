# Twitter/Nest

Sample server-to-server integration between Nest and Twitter.

Allows you to pair up a Twitter account representing a structure with the user's Nest account. Uses a top level actor (`TopActor`) to coordinate updates between a Twitter REST Actor (used for posting updates and DMs), a Twitter Streaming Actor (for subscribing to DMs)
and a Nest actor (`NestActor`) for listening to Firebase updates.

## Install

To get started you'll need a [Twitter API key / access token][twitter-keys], and a [Nest access token][nest-keys].

Copy `src/main/resources/credentials-sample.txt` to `src/main/resources/credentials.txt`, fill in the placeholder values.

## Building

Building is done with [Sbt][sbt] which is available on most platforms.

``` sh
sbt compile
```


Alternatively you can build with [Maven][maven]. The compilation task in this case is done by running:

``` sh
mvn compile
```

You can edit either `build.sbt` or `pom.xml` files in the root of the project in most Java IDEs.

## Running

After you've compiled you can run the application by running the following:

``` sh
sbt run
```

...or if you use maven:
``` sh
mvn exec:java -Dexec.mainClass=com.nestlabs.twest.Main
```


Assuming your config is set up (as described earlier) you should see messages logged to standard output.

## Contributing

Contributions are always welcome and highly encouraged.

See [CONTRIBUTING](CONTRIBUTING.md) for more information on how to get started.

## License

Apache 2.0 - See [LICENSE](LICENSE) for more information.

[sbt]: http://scala-sbt.org/
[maven]: http://maven.apache.org/
[twitter-keys]: https://dev.twitter.com
[nest-keys]: https://developer.nest.com
