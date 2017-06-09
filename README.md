# Help us Cast A Wider .NET!
[![Build Status](https://travis-ci.org/AWiderDotNET/AWiderDotNet.github.io.svg?branch=master)](https://travis-ci.org/AWiderDotNET/AWiderDotNet.github.io)

This is the project / site that supports the domain https://awider.net, in an attempt to foster more involvement in the .NET OSS world.

While there is no code in the repository yet, we hope you'll join us for planning discussions over the in the [issues section](https://github.com/SeanKilleen/AWiderDotNet/issues). We encourage you to start your own topics as well if they're not covered so we can think about how best to bring this project to fruition.

# How to Build this Site

Run `build -target preview`

This project uses [Cake](http://cakebuild.net) to instrument the build and [Wyam](https://wyam.io) as the static site generator. This command will run Wyam via Cake, downloading all the tools and other packages you need.