# Testing with RSpec: A Guided Tutorial

This is a guided tutorial for testing with [RSpec 3](https://github.com/rspec).
It is intended primarily for developers new to both testing and RSpec. However,
any developer using RSpec can still benefit from the content of this tutorial.


## Content Notice

The ideas and thoughts expressed here are not necessarily those of the
[RSpec](https://github.com/rspec) core team. RSpec is a powerful tool which
offers many varied and valid approaches to the same problems. Our content
comprises one set of views on how to utilize RSpec as an effective
communication and specification verification tool.


## How To Use This Tutorial

[This repo](https://github.com/cupakromer/rspec-tutorial) will host the sample
code that is used in the associated
[tutorials](http://aaronkromer.com/blog/categories/rspec-tutorial). Copies of
the tutorial posts are included here under [tutorials](tutorials/) in
[markdown](https://daringfireball.net/projects/markdown/) format.

Each post topic is outlined below under [topics covered](#topics-covered). In
addition to the topic title, a tag link will be included which points to the
last commit for the code associated with that topic. Each subtopic will have a
commit link so that, if you wish, you can follow along as the tutorial is
progresses. These commit messages may also contain addition notes / links which
were not suitable for the main tutorial post.

### Follow Along On Your Own

Awesome initiative!!

We suggest starting with a new repository (our prompt will look like
`[PATH]$`):

```sh
[~]$ mkdir my-rspec-tutorial
[~]$ cd my-rspec-tutorial
[~/my-rspec-tutorial]$ git init
[~/my-rspec-tutorial]$ git add .
[~/my-rspec-tutorial]$ git commit -m "Initial commit."
```

We also suggest setting up a standard Ruby configuration such as
(feel free to copy our files):

  * [`.gitignore`](.gitignore)
  * [`.ruby-version`](.ruby-version)
  * [`Gemfile`](Gemfile)

When you have your configuration setup, add the files, commit, and install the
necessary gems:

```sh
[~/my-rspec-tutorial]$ git add .gitignore .ruby-version Gemfile
[~/my-rspec-tutorial]$ git commit -m "Basic Ruby setup"
[~/my-rspec-tutorial]$ bundle
```

Now simply start going through each of the [topics](#topics-covered).
:thumbsup:

### Follow Along Using This Repo

Great!! We really hope we've provided content in a useful and meaningful way.

To follow along at home clone this repository (our prompt will look
like `[PATH]$`):

```sh
[~]$ git clone https://github.com/cupakromer/rspec-tutorial.git
[~]$ cd my-rspec-tutorial
```

Now simply start going through each of the [topics](#topics-covered). You can
checkout the state of the project at each part by using the associated tag:

```sh
# For example, you are starting with part 1. To see all of the code as it
# appears by the end of the tutorial section:
[~/rspec-tutorial]$ git checkout end-part-1
```

As you read through the associated tutorial post, feel free to browse the code.
Sometimes the same file may change multiple times over the course of the
tutorial. In that case, you can take a look at the commit history to see how
the file evolved. The associated commit hashes are also listed with the
[topics](#topics-covered).

```sh
# Here you want to know FILL_OUT_AFTER_FIRST_POST
[~/rspec-tutorial]$ git log ADD_SHA
```


## Topics Covered

_As new topics are covered, they will be documented here._


## Questions? Wanna chat?

We're really rather friendly! Here are the best places to talk about the
project:

  - Start an [issue on GitHub](https://github.com/cupakromer/rspec-tutorial/issues/new)
  - Try to find us on IRC, we tend to hang out in `#rspec` on Freenode
  - Contact us on Twitter:
    * Aaron Kromer ([@cupakromer](https://twitter.com/cupakromer))


## Contributing

Thinking of contributing back? We :heart: all contributions. Please review our
[contributing guide](CONTRIBUTING.md) for further details.

### Code of Conduct

:purple_heart: Help us keep this learning tutorial open and inclusive. Please
read and follow our [Code of Conduct](CODE_OF_CONDUCT.md). :blue_heart:

### Topic Suggestions

If you just have a suggestion for a topic, or something you wish for us to
cover, please open an
[issue on GitHub](https://github.com/cupakromer/rspec-tutorial/issues/new).
Feel free to apply the `topic` label when submitting.

When submitting topic suggestions, we'd appreciate it if you would include the
following:

  - Short detailed description of the topic (not just the name of an RSpec
    DSL method or general testing topic)
  - A more detailed explanation stating the desired learning goal for the topic
    tutorial; feel free to include multiple learning goals which may be broken
    across tutorials
  - Any example code you may have in mind to demonstrate


## Authors

- [Aaron Kromer](https://github.com/cupakromer)

Thank you to all of our
[Contributors](https://github.com/cupakromer/rspec-tutorial/graphs/contributors).

If you'd like to contribute, please see our
[contribution guidelines](CONTRIBUTING.md) first.


## License

Guided Testing with RSpec: A guided introduction to testing with RSpec 3

Copyright :copyright: 2014  Aaron Kromer

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
