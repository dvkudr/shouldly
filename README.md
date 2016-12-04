![Icon](https://raw.github.com/shouldly/shouldly/master/package_icon.png)

Shouldly
========

[![Build Status](https://ci.appveyor.com/api/projects/status/github/shouldly/shouldly?branch=master&svg=true)](https://ci.appveyor.com/project/shouldly/shouldly) 
[![NuGet](https://img.shields.io/nuget/dt/shouldly.svg)](https://www.nuget.org/packages/Shouldly) 
[![NuGet](https://img.shields.io/nuget/vpre/shouldly.svg)](https://www.nuget.org/packages/Shouldly)
[![Documentation Status](https://readthedocs.org/projects/shouldly/badge/?version=latest)](http://shouldly.readthedocs.org/en/latest/?badge=latest)

[![Join the chat at https://gitter.im/shouldly/shouldly](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/shouldly/shouldly?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) 

Shouldly is an assertion framework which focuses on giving great error messages when the assertion fails while being simple and terse.

This is the old *Assert* way: 

    Assert.That(contestant.Points, Is.EqualTo(1337));

For your troubles, you get this message, when it fails:

    Expected 1337 but was 0

How it **Should** be:

    contestant.Points.ShouldBe(1337);

Which is just syntax, so far, but check out the message when it fails:

    contestant.Points should be 1337 but was 0

It might be easy to underestimate how useful this is. Another example, side by side:

    Assert.That(map.IndexOfValue("boo"), Is.EqualTo(2));    // -> Expected 2 but was 1
    map.IndexOfValue("boo").ShouldBe(2);                    // -> map.IndexOfValue("boo") should be 2 but was 1

**Shouldly** uses the code before the *ShouldBe* statement to report on errors, which makes diagnosing easier.

Read more about Shouldly and its features at [http://docs.shouldly-lib.net/](http://docs.shouldly-lib.net/).

## Installation

You can install Shouldly by copying and pasting the following command into your Package Manager Console within Visual Studio (Tools > NuGet Package Manager > Package Manager Console).

`Install-Package Shouldly`

## Contributing
Contributions to Shouldly are very welcome. For guidance, please see [CONTRIBUTING.md](CONTRIBUTING.md)

## Pre-requisites for running on build server
Shouldly uses the source code to make its error messages better. Hence, on the build server you will need to have the "full" pdb files available where the tests are being run. 

What is meant by "full" is that when you set up your "release" configuration in Visual Studio and you go to Project Properties > Build > Advanced > Debug, you should set it to "full" rather than "pdb-only". 

## History Change
A test results database (~50mb) got accidentally committed in a972872888925205c9655cb540455d23d1891148, we removed this from history.
The commit was only in master for <24 hours but if you happened to pull then you may need to reset master to get back in line.

## Icon
[Star](https://thenounproject.com/term/star/20931/) created by [Luboš Volkov](https://thenounproject.com/Lubo%C5%A1%20Volkov/) from The Noun Project.

## Currently maintained by
 - [Jake Ginnivan](https://github.com/JakeGinnivan)
 - [Joseph Woodward](https://github.com/JosephWoodward)

If you are interested in helping out, jump on [gitter](https://gitter.im/shouldly/shouldly) and have a chat.

## Brought to you by
 - Dave Newman
 - Xerxes Battiwalla
 - Anthony Egerton
 - Peter van der Woude
 - Jake Ginnivan
