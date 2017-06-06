# Help us Cast A Wider .NET!
![Travis ci build status](https://travis-ci.org/AWiderDotNET/AWiderDotNet.github.io.svg?branch=master)

This is the project / site that supports the domain https://awider.net, in an attempt to foster more involvement in the .NET OSS world.

While there is no code in the repository yet, we hope you'll join us for planning discussions over the in the [issues section](https://github.com/SeanKilleen/AWiderDotNet/issues). We encourage you to start your own topics as well if they're not covered so we can think about how best to bring this project to fruition.

# How to Build this Site

* Install Ruby (2.3.x is what we're using)
* Install the bundler gem: `gem install bundler`
* Head to the root directory in your command prompt
* Run `bundle install`. The github pages gems will install.
* Run `bundle exec jekyll serve --config _config.yml,_config.dev.yml` . This will serve the page at `http://localhost:4000`
 * If you omit the `--config` references, all URLs will reference the prod site, which may be confusing.
 * This reference means that the standard `_config.yml` is used first, and then overridden with the values in `_config.dev.yml`.
If you run into problems, add an issue in this repo and we'll figure it out.

## Troubleshooting: Regeneration throws an SSL Error
Sean [Ran into this problem](https://github.com/github/pages-gem/issues/399#issuecomment-280205210).

Here's the fix on Windows, per that thread (note -- requires a restart):

* Go to GitHub and [generate a personal access token](https://github.com/settings/tokens)
 * It just needs public access
 * Don't forget to copy the token text!
* Create a system environment variable called `JEKYLL_GITHUB_TOKEN` and set the value to the token text
* Create a system environment variable called `SSL_CERT_FILE` and set the value to the full path of the `cacert.pem` file (found in the root directory of this repo)
* Restart your machine. 

This should remove this error when building the repo. (ugh, sorry about that)