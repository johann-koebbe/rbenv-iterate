### Execute a command in multiple, specific rbenv rubies.

```bash
  Usage: rbenv exec [-i list-or-regex] [-e list-or-regex] [-q] command

  Examples:

  Exclude all JRubies using a regular expression:
  $ rbenv exec -i /^jruby/ command

  Include only 2.1.6 and 2.2.2 using a comma-separated list (no spaces):
  $ rbenv exec -i '2.1.6,2.2.2' command
```

This plugin is very similar to [rbenv-each](https://github.com/rbenv/rbenv-each) and
[rbenv-only](https://github.com/Rodreegez/rbenv-only), except that it is implemented in Ruby and provides for excluding
and the use of regular expressions.

Tested in MRI 1.9.3/2.1/2.2 and JRuby 1.7.

