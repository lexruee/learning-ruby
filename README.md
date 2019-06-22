# Learning Ruby

Playground repository to learn the Ruby Programming Platform in more detail.

## Ruby version manager

There are multiple options for managing ruby version on a system.
Some popular Ruby version managers are:

    * rvm
    * rbenv
    * asdf-vm
    
    
### asdf-vm

Installation:

```
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.7.2
echo -e '\n. $HOME/.asdf/asdf.sh' >> ~/.zshrc
echo -e '\n. $HOME/.asdf/completions/asdf.bash' >> ~/.zshrc
source ~/.zshrc
```

Install ruby and setup the global ruby version:

``` 
asdf plugin-add ruby
asdf install ruby 2.6.3
asdf global ruby 2.6.3
```

## Rubygems

Rubygems is the main package manager for the Ruby programming platform.

For more details see `gem --help`:

```
gem --help
RubyGems is a sophisticated package manager for Ruby.  This is a
basic help message containing pointers to more information.

  Usage:
    gem -h/--help
    gem -v/--version
    gem command [arguments...] [options...]

  Examples:
    gem install rake
    gem list --local
    gem build package.gemspec
    gem help install

  Further help:
    gem help commands            list all 'gem' commands
    gem help examples            show some examples of usage
    gem help gem_dependencies    gem dependencies file guide
    gem help platforms           gem platforms guide
    gem help <COMMAND>           show help on COMMAND
                                   (e.g. 'gem help install')
    gem server                   present a web page at
                                 http://localhost:8808/
                                 with info about installed gems
  Further information:
    http://guides.rubygems.org
```


## bundler

Bundler is the tool to manage rubygems dependency in a ruby-based project.

> Bundler provides a consistent environment for Ruby projects by tracking 
> and installing the exact gems and versions that are needed.

Resources:

 * [Bundler's Purpose and Rationale](https://bundler.io/rationale.html)
 * [Workflow](https://bundler.io/rationale.html#summary)


Installation:

``` 
gem install bundler
```

For more details see `bundler --help`:


``` 
bundler --help
BUNDLE(1)                                                                                                                                                                                                                                                BUNDLE(1)

NAME
       bundle - Ruby Dependency Management

SYNOPSIS
       bundle COMMAND [--no-color] [--verbose] [ARGS]

DESCRIPTION
       Bundler manages an application's dependencies through its entire life across many machines systematically and repeatably.

       See the bundler website https://bundler.io for information on getting started, and Gemfile(5) for more information on the Gemfile format.

OPTIONS
       --no-color
              Print all output without color

       --retry, -r
              Specify the number of times you wish to attempt network commands

       --verbose, -V
              Print out additional logging information

BUNDLE COMMANDS
       We divide bundle subcommands into primary commands and utilities:

PRIMARY COMMANDS
       bundle install(1) bundle-install.1.html
              Install the gems specified by the Gemfile or Gemfile.lock

       bundle update(1) bundle-update.1.html
              Update dependencies to their latest versions

       bundle package(1) bundle-package.1.html
              Package the .gem files required by your application into the vendor/cache directory

       bundle exec(1) bundle-exec.1.html
              Execute a script in the current bundle

       bundle config(1) bundle-config.1.html
              Specify and read configuration options for Bundler

       bundle help(1)
              Display detailed help for each subcommand

UTILITIES
       bundle add(1) bundle-add.1.html
              Add the named gem to the Gemfile and run bundle install

       bundle binstubs(1) bundle-binstubs.1.html
              Generate binstubs for executables in a gem

       bundle check(1) bundle-check.1.html
              Determine whether the requirements for your application are installed and available to Bundler

       bundle show(1) bundle-show.1.html
              Show the source location of a particular gem in the bundle

       bundle outdated(1) bundle-outdated.1.html
              Show all of the outdated gems in the current bundle

       bundle console(1)
              Start an IRB session in the current bundle

       bundle open(1) bundle-open.1.html
              Open an installed gem in the editor

       bundle lock(1) bundle-lock.1.hmtl
              Generate a lockfile for your dependencies

       bundle viz(1) bundle-viz.1.html
              Generate a visual representation of your dependencies

       bundle init(1) bundle-init.1.html
              Generate a simple Gemfile, placed in the current directory

       bundle gem(1) bundle-gem.1.html
              Create a simple gem, suitable for development with Bundler

       bundle platform(1) bundle-platform.1.html
              Display platform compatibility information

       bundle clean(1) bundle-clean.1.html
              Clean up unused gems in your Bundler directory

       bundle doctor(1) bundle-doctor.1.html
              Display warnings about common problems

       bundle remove(1) bundle-remove.1.html
              Removes gems from the Gemfile

PLUGINS
       When running a command that isn't listed in PRIMARY COMMANDS or UTILITIES, Bundler will try to find an executable on your path named bundler-<command> and execute it, passing down any extra arguments to it.

OBSOLETE
       These commands are obsolete and should no longer be used:

       •   bundle cache(1)

       •   bundle show(1)
```

