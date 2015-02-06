---
layout: post
title:  "Open Source Opener"
date:   2015-02-05 21:58:32
categories: Open Source, Javascript
---

We've had a little something up our sleeve for over a year now. We call it [BBCore](http://github.com/BombBomb/BBCore).
BBCore is a Javascript library that encapsulates [BombBomb's API](http://bombbomb.com/api) so web developers can easily embed video recorders, send emails, manage contacts and more with nice javascript calls. We've used internally as a middle-tier in our [Chrome Extension](https://chrome.google.com/webstore/detail/bombbomb/mfldbojpjpgjlphijlbgefdjebkhdjom?hl=en), and externally in helping parters install BombBomb technology into their software. What started as a little abstraction layer has grown up.

###How do you open source?
Off the top of our heads we came up with the following task list:

1. Open source on Github
2. Install a testing framework
3. Auto-Document the Javascript
4. Create an example page
5. Configure a build/release process


### Github and Git
BombBomb has historically been a Subversion shop. It's served us well, but Git's the state of the art. We've dabbled in handful of small, lightly collaborative git environments, but BBCore had three developers working hard and fast together. Our belief was git did a much defter job of keeping developers out of [merge hell](http://stackoverflow.com/questions/16358418/how-to-avoid-merge-commit-hell-on-github-bitbucket). We found merge-drama to be largely alive and well when two or three people are banging around in a file together. Courtesy still win the day: communicate closely about larger changes and sync up often.

### Ecosystem: Grunting at Travis
[![Build Status](https://travis-ci.org/bombbomb/BBCore.svg?branch=master)](https://travis-ci.org/bombbomb/BBCore)
[![Code Climate](https://codeclimate.com/github/bombbomb/BBCore/badges/gpa.svg)](https://codeclimate.com/github/bombbomb/BBCore)
[![Test Coverage](https://codeclimate.com/github/bombbomb/BBCore/badges/coverage.svg)](https://codeclimate.com/github/bombbomb/BBCore)

The most fun we had with this project was discovering and getting into the javascript build world of [Grunt](http://gruntjs.com/) and [Travis CI](https://travis-ci.org/bombbomb/BBCore). There's a plugin for everything! It took about two days to get a build solidified that:
[auto-generated our documentation](http://jsdox.org/) (jsdox), 
[ran tests with code coverage](http://karma-runner.github.io/) (Karma, Jasmine and Code Climate),
[checked code cleanliness and complexity](http://jshint.com/) (JSHint),
minified and shipped our new project. 

### Simplicity through Complexity