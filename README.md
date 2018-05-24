# prettier-ruby

This is a work in progress plugin for prettier that supports the Ruby programming language. Under the hood it uses the [`ripperjs`](https://github.com/kddeisz/ripperjs) package (which in turn uses Ruby's own `ripper` library) which allows this package to maintain parity with the existing Ruby parser.

## Getting started

Install the dependencies by running `yarn` in the root of the repository. You can then pretty print a ruby source file by running `yarn print [PATH]`.

## Options

Below are the options (from [`src/index.js`](src/index.js) that `prettier-ruby` currently supports:

* `inlineConditionals` - When it fits on one line, allow if and unless statements to use the modifier form.
* `inlineLoops` - When it fits on one line, allow while and until statements to use the modifier form.
* `preferSingleQuotes` - When double quotes are not necessary for interpolation, prefer the use of single quotes for string literals.

## Known limitations

There are still a couple of node types to support, listed below. Additionally, `prettier-ruby` is still dropping comments because the `ripperjs` package doesn't yet have support for them.

- [ ] BEGIN
- [ ] END
- [ ] alias_error
- [ ] arg_ambiguous
- [ ] assign_error
- [ ] class_name_error
- [ ] command_call
- [ ] excessed_comma
- [ ] heredoc_dedent
- [ ] magic_comment
- [ ] operator_ambiguous
- [ ] param_error
- [ ] parse_error
- [ ] string_dvar
- [ ] var_alias
