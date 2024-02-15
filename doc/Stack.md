# Tech Stack

The main stack of technologies:

* OS:
  [GNU/Linux](https://en.wikipedia.org/wiki/Linux) or
  [MacOS](https://en.wikipedia.org/wiki/MacOS) or
  [Windows](https://en.wikipedia.org/wiki/Microsoft_Windows)
  (with or without
  [WSL](https://learn.microsoft.com/en-us/windows/wsl/))
* Languages:
  [JavaScript](https://developer.mozilla.org/en-US/docs/Glossary/JavaScript)/[TypeScript](https://www.typescriptlang.org)
  (with
  [JSX](https://react.dev/learn/writing-markup-with-jsx)/[TSX](https://react.dev/learn/typescript#typescript-with-react-components)),
  [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML),
  [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)/[SCSS](https://sass-lang.com/guide/)
* RunTime:
  [Node.js](https://nodejs.org/en)
  (non-browser JavaScript runtime, with
  [npm](https://docs.npmjs.com/about-npm),
  [npx](https://docs.npmjs.com/cli/v10/commands/npx)
  tools)
* RunTime Manager:
  [pnpm](https://pnpm.io/cli/env)
  (instead of
  [nvm](https://github.com/nvm-sh/nvm) or
  [nvm-windows](https://github.com/coreybutler/nvm-windows))
* Package Manager:
  [pnpm](https://pnpm.io/cli/add)
  (instead of
  [npm](https://nodejs.org/en/learn/getting-started/an-introduction-to-the-npm-package-manager)
  but still using the
  [npm](https://www.npmjs.com/)
  registry)
* Meta-Framework:
  [Next.js](https://nextjs.org/)
  (no longer using the legacy
  [create-react-app](https://legacy.reactjs.org/docs/create-a-new-react-app.html)
  but
  [create-next-app](https://nextjs.org/docs/pages/api-reference/create-next-app)
  instead
  )
* Frontend Framework:
  [React.js](https://react.dev)
* Editor/IDE:
  [VSCode](https://code.visualstudio.com/) (Micosoft Visual Studio Code)
  with various
  [extensions](https://code.visualstudio.com/docs/editor/extension-marketplace)
* Linting:
  * Markdown linting with
    [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
  * JavaScript/TypeScript linting with [ESLint](https://eslint.org) and
    [Stylistic](https://eslint.style/) (where stylistic is integrated in the
    config file `.config/.eslintrc.json`)
  * CSS/SCSS linting with [Stylelint](https://stylelint.io) (validation) and
    [Prettier](https://prettier.io/) (formatting)
  * JSON linting with [Prettier](https://prettier.io/)
  * Bash shell linting with
    [ShellCheck](https://marketplace.visualstudio.com/items?itemName=timonwong.shellcheck)
  * Python linting with
    [Pylint](https://marketplace.visualstudio.com/items?itemName=ms-python.pylint)
