# Contributing

We'd love for you to contribute back to our tutorial series making it even
better. The following are the guidelines we'd appreciate that you follow. Don't
forget to have fun learning!


## Project Goals

This guided tutorial is an attempt to introduce newer developers to strong
testing practices while using RSpec. The tutorial is designed to introduce
various features of the RSpec 3 testing tool in an manner which is:

  - approachable; tutorials are easy to follow and progress through
  - manageable; RSpec features are introduced gradually in a manner which
    progressively improves on prior explained features and topics
  - promoting of what we consider strong testing practices

This tutorial series is primarily intended for developers new to both testing
and RSpec. Even though that is our initial target audience, any developer using
RSpec can still derive benefit from the content.


## Code of Conduct

Help us keep this learning tutorial open and inclusive. Read and follow our
[code of conduct](CODE_OF_CONDUCT.md).


## Project Status

### 2014-02-16

This is a new project. We are just getting off the ground.


## Have a Question or Problem?

We're really rather friendly! Here are the best places to talk about the
project:

  - Start an [issue on GitHub](https://github.com/cupakromer/rspec-tutorial/issues/new)
  - Try to find us on IRC, we tend to hang out in `#rspec` on Freenode
  - Contact us on Twitter:
    * Aaron Kromer ([@cupakromer](https://twitter.com/cupakromer))


## Interested in New Topics?

If you have a suggestion for a topic, or something you wish for us to cover,
please open an
[issue on GitHub](https://github.com/cupakromer/rspec-tutorial/issues/new).
Feel free to apply the `topic` label when submitting. Before submitting your
topic idea search the archive, we may have already discussed it.

When submitting topic suggestions, we'd appreciate it if you would include the
following:

  - Short detailed description of the topic (not just the name of an RSpec
    DSL method or general testing topic)
  - A more detailed explanation stating the desired learning goal for the topic
    tutorial; feel free to include multiple learning goals which may be broken
    across tutorials
  - Any example code you may have in mind to demonstrate

Since topics tend to be fairly major changes, we appreciate you opening an
issue first, before spending time writing up the content. We ask this so that
we can properly coordinate how the topic should fit into the existing tutorial
series.


## Version Support

All submissions which include code samples or reference code **must** work with
Ruby 2.1.0 or newer. As well as, RSpec 3.0.0.beta1 or newer.

  - Ruby >= 2.1.0
  - RSpec >= 3.0.0.beta1


## Submitting Your Changes

You've got something you want to contribute back. Huge thank you!

Our general steps for contributing back to the project are:

  1. Search [GitHub](https://github.com/cupakromer/rspec-tutorial/pulls) for an
     open or closed Pull Request that relates to your submission. You don't
     want to duplicate effort.

  2. Fork the repo.

  3. Create a feature branch (`git checkout -b my-new-feature`)

  4. Run the specs. We only take pull requests with passing specs, and it's
     great to know that you have a clean slate: `bundle && rspec`

  5. Add your content. This includes:
    - Associated tutorial
    - Relevant code
    - Specs for all code changes; only refactoring and documentation changes
      require no new specs

  6. Verify you've adhered to our [coding style guide](#code-syntax)

  7. Commit your changes with a descriptive commit message; check our
     [tips for creating good commit messages](#commit-messages)

  8. Push the branch to _your_ fork (`git push origin my-new-feature`)

  9. Create new [Pull Request](https://github.com/cupakromer/rspec-tutorial/compare/)

### Submission Feedback

We'll do our best to comment on all pull requests in a timely manner. When we
leave a comment, we may make some suggestions, changes, and/or improvements. It
is possible we may also leave other general feedback on how we feel the request
fits in with the rest of the project goals.

### Code Syntax

  * Two space indents, no tabs

  * No trailing whitespace

  * Blank lines should not have any other whitespace

  * Prefer `&&`/`||` over `and`/`or`

  * Use parenthesis, without whitespace, for method definitions which take
    arguments:

    - Bad: `def do_something with_object`
    - Bad: `def do_something( with_object )`
    - Good: `def do_something(with_object)`

  * When sending messages, always use parenthesis if the return value is
    meaningful and an argument is passed, parenthesis should not contain buffer
    whitespace:

    - Bad: `tmp = a_string.gsub /test/, "check"`
    - Bad: `tmp = a_string.gsub( /test/, "check" )`
    - Good: `tmp = a_string.gsub(/test/, "check")`
    - Good: `tmp = a_string.upcase`
    - OK - Non-meaningful return: `a_string.gsub! /test/, "check"`

  * When using blocks:

    - Always use the bracket `{`...`}` style for meaningful return values; do
      not separate the message and left bracket `{` with whitespace:
      ```ruby
      # Bad - Whitespace after `select`
      evens = numbers.select { |num| num.even? }

      # Good
      evens = numbers.select{ |num| num.even? }
      sum_of_squares = evens.reduce(0){ |sum, num|
        sum + (num * num)
      }
      ```

    - Always use the `do`...`end` style for non-meaningful return values:
      ```ruby
      commands.each do |command|
        puts "Calling #{command}"
        command.call
      end
      ```

    - Do **not** use the bracket `{`...`}` style for non-meaningful one liners;
      use the `do`...`end` style spread across multiple lines:
      ```ruby
      # Bad
      numbers.each{ |num| puts num }

      # Good
      numbers.each do |num|
        puts num
      end
      ```

  * Put whitespace around assignments: `a = b` and **not** `a=b`

  * Follow any additional conventions you see used in the source already

### Commit Messages

For any git project, some good rules for commit messages are:

  * the first line is commit summary, 50 characters or less
  * followed by an empty line
  * followed by an explanation of the commit, wrapped to 72 characters

For more on commit messages see:

  * [A Note About Git Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
  * [Every line of code is always documented](http://mislav.uniqpath.com/2014/02/hidden-documentation/)

### A Note on Pull Requests

That's it! Again, big thank you for your contribution! :heart:

While the patch is being reviewed, we may ask that you make additional changes.
We'll provide further guidance at this point on a case-by-case basis. We'll use
the Pull Request for all additional communications.

After the patch has been merged, it is safe for you to delete your associated
feature branch. Please don't delete the branch before we've merged, or closed,
the Pull Request. It will make submitting any necessary changes easier for you
and us.

Additionally, after we've merged the patch, you can then pull down the changes
from the main upstream repository:

  * Delete your remote feature branch on Github:

    ```shell
    git push origin --delete my-fix-branch
    ```

  * Check out your local master branch:

    ```shell
    git checkout master -f
    ```

  * Delete your local feature branch:

    ```shell
    git branch -D my-fix-branch
    ```

  * Update your master with the latest upstream version:

    ```shell
    git pull --ff upstream master
    ```

# :heart: THANK YOU! :heart:
