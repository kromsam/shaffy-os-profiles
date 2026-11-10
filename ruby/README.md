# ruby

Ruby for the editor and for agents:

- **mise** installs the latest precompiled Ruby and, after every `mise install`, the
  `ruby-lsp` gem into it. A project's `.ruby-version` picks its own Ruby.
- **LazyVim** loads its Ruby extra, which uses that `ruby-lsp`.
- **Claude Code** gets the `ruby-lsp` plugin from Anthropic's marketplace repository, which
  also declares the language server.

What runs code: the mise fragment (it installs Ruby and runs `gem install` after each
install), the LazyVim extra and the Claude Code plugin. Nothing is installed as root.

`./bin/shaffy update` installs the Ruby after you list the profile and apply the home.
Gems your projects need, and the system libraries they build against, stay in your own
supplement.
