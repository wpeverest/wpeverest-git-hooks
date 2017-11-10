# WPEverest Git Hooks

Collection of WPEverest core git hooks.

## Installation

```bash
composer require wpeverest/wpeverest-git-hooks
```

## Usage

Include the follow lines into the project's `composer.json`:

```
    "scripts": {
        "pre-update-cmd": "WPEverest\\GitHooks\\Hooks::preHooks",
        "pre-install-cmd": "WPEverest\\GitHooks\\Hooks::preHooks",
        "post-update-cmd": "WPEverest\\GitHooks\\Hooks::postHooks",
        "post-install-cmd": "WPEverest\\GitHooks\\Hooks::postHooks"
    }
```

### Manual setup (optional)

By default should already run all commands from composer `scripts` when installed, but if necessary run it manually is possible with the follow commands:

```bash
composer run-script pre-update-cmd
composer run-script post-update-cmd
```

## Release history

- 2017-11-10 - 1.0.1 - Removed list of ignored directories.
- 2017-10-03 - 1.0.0 - Initial release.

## Sources

Inspired by:

- <https://github.com/juizmill/git-hooks>
- <https://github.com/smgladkovskiy/phpcs-git-pre-commit>
