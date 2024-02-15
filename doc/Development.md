# Development

This repo is designed for usage with the following IDE (integrated development
environment), configurations, and extensions.

The editor/IDE [VSCode](https://code.visualstudio.com/) (aka "Code", Microsoft
Visual Studio Code) can perform automatic linting (syntax and style flagging and
enforcement / correction) and type-checking, as well as many other useful tasks
and functionalities, some provided by
[extensions](https://code.visualstudio.com/docs/editor/extension-marketplace)
that can be installed into the editor.

Included in this repo is the workspace settings (at `.vscode/settings.json`)
that controls the configuration of VSCode while working in this repo/project.

Note: A separate user settings file can control the configuration globally for a
user on a particular machine, and those user settings can be partly or wholy
overridden by the workspace settings file.

You may need to install VSCode version 1.85 or greater for it to accept the
`settings.json` file as it is written. If you already have VSCode installed, you
might need to [uninstall](https://code.visualstudio.com/docs/setup/uninstall)
to then [download](https://code.visualstudio.com/Download) and install the
latest version.

With VSCode installed, you can install these VSCode extensions to enable linting
and gain other useful features:

* Linting
  * `DavidAnson.vscode-markdownlint`
  * `esbenp.prettier-vscode`
  * `dbaeumer.vscode-eslint`
  * `stylelint.vscode-stylelint`
  * `timonwong.shellcheck`
  * `ms-python.pylint` (not used but referenced in `settings.json`)
* General
  * `eamodio.gitlens`
  * `ybaumes.highlight-trailing-white-spaces`
* Recommended Utility
  * `pucelle.vscode-css-navigation`
  * `compulim.indent4to2`

## ESLint and Stylelint

Besides running [ESLint](https://eslint.org/) and
[Stylelint](https://stylelint.io/) automatically when viewing and editing files
in VSCode, you can also run each of them in the shell/terminal.

In the terminal, to run linting on many files and view issues with the files,
change directory into the root project folder (`react-next-ts`) and run the
following commands:

* `pnpm exec eslint app --ext .ts,.js,.tsx`
* `pnpm exec stylelint "**/*.{css,scss}" --ignore-pattern ".next/*"`

If there are no errors or warnings, there will be no output.

To actually fix, use the option `--fix` with a command.  (With ESLint you can
also use `--fix-dry-run` for a simulation).

For more help:

* ESLint: use `pnpm exec eslint --help` or look
  [here](https://eslint.org/docs/latest/use/command-line-interface).
* Stylelint: see more options [here](https://stylelint.io/user-guide/options/).

## Prettier

* `pnpm exec prettier --help`

This command does not seem to give user friendly output:

* `pnpm exec prettier "app/*.{css,scss}" "app/**/*.{css,scss}"`

Here are some other failed ideas:

* `pnpm exec prettier "app/*.{css,scss}" "app/**/*.{css,scss}" --log-level warn`
* `pnpm exec prettier "app/*.{css,scss}" "app/**/*.{css,scss}" --debug-check`
