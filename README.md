# Scala.js, a Scala to JavaScript compiler

This project aims at providing a Scala to JavaScript compiler, so that one
can write the client-side of a Web application in Scala, and have it compiled
into JavaScript code.

## Mailing list

[https://groups.google.com/forum/?fromgroups#!forum/scala-js](https://groups.google.com/forum/?fromgroups#!forum/scala-js)

## Get it

Get the code with git. Beware that this repo contains two submodules, which
you need to clone too. So after cloning this repo, cd into it and do:

    $ git submodule init
    $ git submodule update

## Compile and publish it locally (install)

Scala.js uses [sbt](http://www.scala-sbt.org/) for its build process.
In order to use it locally, you need to 1) package the Scala.js runtime, and
2) publish the compiler, library and sbt plugin locally.

Don't worry, this is super-easy:

    sbt> package-js
    sbt> publish-local

## Test the examples

You can compile the example applications with:

    sbt> examples/package-js

Then, you can "execute" them by opening their respective HTML files in your
favorite browser.

Currently, two examples are provided:

*   `examples/helloworld/helloworld.html`, saying Hello World in four different
    ways (using DOM or jQuery, and using the untyped or typed interface to
    JavaScript).
*   `examples/reversi/reversi.html`, an implementation of a
    [Reversi](http://en.wikipedia.org/wiki/Reversi) game. Note that it uses the
    HTML5 Canvas element, so it won't work with Internet Explorer 8 or below.

## Get started with your own project

We provide an
[exampe application](https://github.com/sjrd/scala-js-example-app) which you
can fork to kick off your own project. Its readme provides further
explanations on how to do so.

## License

Scala.js is distributed under the
[Scala License](http://www.scala-lang.org/node/146).
