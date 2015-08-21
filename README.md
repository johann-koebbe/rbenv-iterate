### Description

Execute a command in multiple, specific rbenv rubies.

### Usage

```bash
Usage: rbenv iterate [-i filter] [-e filter] [-q] [-d] command

Options:

-i filter / --include=filter     Comma-separated list or regular expression of versions to include.
-e filter / --exclude=filter     Comma-separated list or regular expression of versions to exclude.
-q / --quiet                     Do not echo current version during iteration.
-d / --dry-run                   Echo the command instead of executing it.

Examples:

Exclude all JRubies using a regular expression:
$ rbenv iterate -e /^jruby/ command

Include only 2.1.6 and 2.2.2 using a comma-separated list (no spaces):
$ rbenv iterate -i 2.1.6,2.2.2 command
```

### Installation

```bash
$ mkdir -p $RBENV_ROOT/plugins
$ git clone git@github.com:phillip-koebbe-fidelity/rbenv-iterate.git $RBENV_ROOT/plugins/rbenv-iterate
```

### Notes

This plugin is very similar to [rbenv-each](https://github.com/rbenv/rbenv-each) and
[rbenv-only](https://github.com/Rodreegez/rbenv-only), except that it provides for excluding
and the use of regular expressions.

Where an argument is required, the long version of an option requires an equal sign. A space will not work.

```command``` can be surrounded by quotes or not. Your choice.

Excluding overrides including, so if you specify

```bash
$ rbenv iterate -i /^jruby/ -e jruby-9.0.0.0 gem install some-gem
```

some-gem will be installed for all versions of JRuby *except* jruby-9.0.0.0.
