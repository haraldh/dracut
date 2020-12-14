# Dracut Developer Guidelines

## git

### Commit Messages

Commit messages should answer these questions:

* What?: a short summary of what you changed in the subject line.
* Why?: what the intended outcome of the change is (arguably the most important piece of information that should go into a message).
* How?: if multiple approaches for achieving your goal were available, you also want to explain why you chose the used implementation strategy.
  Note that you should not explain how your change achieves your goal in your commit message.
  That should be obvious from the code itself.
  If you cannot achieve that clarity with the used programming language, use comments within the code instead.

The commit message is primarily the place for documenting the why.

Commit message titles should follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).

Format is `<type>[optional scope]: <description>`, where `type` is one of:

* fix: A bug fix
* feat: A new feature
* perf: A code change that improves performance
* refactor: A code change that neither fixes a bug nor adds a feature
* style: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
* test: Adding missing tests or correcting existing tests
* docs: Documentation only changes
* revert: Reverts a previous commit
* chore: Other changes that don't modify src or test files
* build: Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)
* ci: Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)

`scope` should be the module name (without numbers) or:

* cli: for the dracut command line interface
* rt: for the dracut initramfs runtime logic
* functions: for general purpose dracut functions

Commit messages are checked with [Commisery](https://github.com/tomtom-international/commisery).
