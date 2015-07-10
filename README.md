### Description

Execute a command in multiple, specific rbenv rubies.

### Usage

```bash
  Usage: rbenv iterate [-i list-or-regex] [-e list-or-regex] [-q] 'command'

  Examples:

  Exclude all JRubies using a regular expression:
  $ rbenv iterate -e /^jruby/ 'command'

  Include only 2.1.6 and 2.2.2 using a comma-separated list (no spaces):
  $ rbenv iterate -i '2.1.6,2.2.2' 'command'
```

### Installation

```bash
$ mkdir -p $RBENV_ROOT/plugins
$ git clone git@github.com:phillip-koebbe-fidelity/rbenv-iterate.git $RBENV_ROOT/plugins/rbenv-iterate
```

### Notes

This plugin is very similar to [rbenv-each](https://github.com/rbenv/rbenv-each) and
[rbenv-only](https://github.com/Rodreegez/rbenv-only), except that it is implemented in Ruby and provides for excluding
and the use of regular expressions.

Tested in MRI 1.9.3/2.1/2.2 and JRuby 1.7.

