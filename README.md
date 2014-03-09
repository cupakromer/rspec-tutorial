# Testing with RSpec: A Guided Tutorial

This is a guided tutorial for testing with [RSpec 3](https://github.com/rspec).
It is intended primarily for developers new to both testing and RSpec. However,
any developer using RSpec can still benefit from the content of this tutorial.

There's lots of information out there on testing Ruby. A common question we
hear is: _"Which testing framework should I use?"_ At the end of the day, it
doesn't really matter. Pick what makes you happy. Or what your co-workers /
programming pairs are most familiar; this will make asking for help easier.
For us, the tool we enjoy is [RSpec](http://rubygems.org/gems/rspec). One
reason we enjoy RSpec is how it allows us to use a more natural language when
writing our tests.

The usually follow up question is: _"What do I test and how do I do it?"_ Our
goal with this tutorial is to answer these questions. Additionally, we hope to
provide you with a set of skills and tools that can extend to languages and
practices beyond just Ruby and RSpec.


## Content Notice

The ideas and thoughts expressed here are not necessarily those of the
[RSpec](https://github.com/rspec) core team. RSpec is a powerful tool which
offers many varied and valid approaches to the same problems. Our content
comprises one set of views on how to utilize RSpec as an effective
communication and specification verification tool.


## Software Versions

We are using Ruby 2.1+ and RSpec 3 for this tutorial.

If you do not have Ruby 2.1+ installed, we suggest you consider installing it.
There are many different version managers available to assist with this
process.

If you are new to all of this, the following resources provide step-by-step
guides on installing Ruby:

  * [Setup recipe for Rails Girls](http://guides.railsgirls.com/install/)
  * [RailsBridge Installfest](http://docs.railsbridge.org/installfest/installfest)


## Assumptions About Your Environment and Knowledge

In general we assume you don't know anything about RSpec. We do assume you have
some knowledge of:

  * Ruby
  * Bundler and Ruby gems
  * The command line
  * Git
  * A code editor

We also assume you have everything, except RSpec, installed and setup.

### Regarding Ruby

Since we will assume you have at least a **basic level** of knowledge regarding
the Ruby programming language; we will not be diving too deep into its various
idioms and syntaxes. We will occasionally provide additional details about Ruby
specifics as they pertain to using RSpec.

If you are new to Ruby, we suggest you stop for a bit and learn a bit about the
language itself. The following resources provide some good hands on interactive
experience for beginners.

  * [Try Ruby](http://tryruby.org)
  * [Codecademy's Ruby Tracks](http://www.codecademy.com/tracks/ruby)
  * [Ruby Monky Primers](https://rubymonk.com/)

The list of resource available for learning Ruby are constantly updating. We
suggest you search the web for additional resources as you encounter topics
you may not be familiar with.

### Regarding The Command Line

We won't be doing anything complicated with the command line. However, if the
command line is totally new to you, stop for a bit and check out these
introduction resources:

  * [The Command Line Crash Course](http://cli.learncodethehardway.org/book/)
  * [A Command Line Primer for Beginners](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything)

### Regarding Git

We use `git` primarily as a tool for delivering this content to you. Most of
the tutorials and code samples will not mention or use `git` at all. However,
if `git` is new to you, we suggest going through the free `git` course from
[GitHub](https://github.com): http://try.github.io/


## How To Use This Tutorial

[This repo](https://github.com/cupakromer/rspec-tutorial) will host the sample
code that is used in the associated
[tutorials](http://aaronkromer.com/blog/categories/rspec-tutorial). Copies of
the tutorial posts are included here under [tutorials](tutorials/) in
[markdown](https://daringfireball.net/projects/markdown/) format.

Each post topic is outlined below under [topics covered](#topics-covered). In
addition to the topic title, a
[tag](https://github.com/cupakromer/rspec-tutorial/tags) link will be included.
The tag points to the last commit for the code associated with that topic. Each
subtopic will also have a commit link so that, if you wish, you can follow the
code evolution as the tutorial progresses. Addition notes / links which were
not suitable for the main tutorial, but may interest more experienced
developers, will normally be included in the commit messages.

Most of the tutorials are designed to build on the information and code
provided in previous sections. Our recommendation is to go through the
tutorials in the order presented for maximum benefit. We strongly suggest you
follow this recommendation if you are on the newer side of Ruby and/or RSpec.

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
It is likely that the same file will change multiple times over the course of
the tutorial. You can follow each individual change by reviewing the
[commit history](http://git-scm.com/book/en/Git-Basics-Viewing-the-Commit-History).
The main things the history will show are:

  * What file changes were made at each step
  * Additional annotations with further resources on the topic or historical
    notes regarding versions in the commit messages

For your reference, we've put the associated commit hashes next to the
[topics](#topics-covered).

```sh
# For example, to see more about FILL_OUT_AFTER_FIRST_POST
[~/rspec-tutorial]$ git log -p COMMIT_HASH
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
