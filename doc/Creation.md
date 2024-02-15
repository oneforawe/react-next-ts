# Creation of the Repo

See the [web-dev](./WebDev.md) and [development](./Development.md) notes for the
initial setup before executing the commands below.

Note: The commands below were not executed in the order shown, but the order
shown is more organized and should be appropriate.

## Initialize

The commands below were used to initialize the repository.

See references for [pnpm-create](https://pnpm.io/cli/create) and
[create-next-app](https://nextjs.org/docs/pages/api-reference/create-next-app).
You can also see some help by executing `pnpm create next-app --help`

* Create initial React/Next app. Either:  
  (interactive) `pnpm create next-app`  
  (automatic) `pnpm create next-app react-next-ts --use-pnpm --typescript --eslint --app --no-src-dir --no-tailwind --import-alias '@/*'`
* Enter repo.  
  `cd react-next-ts`
* Confirm functionality.  
  `pnpm run dev` and observe <http://localhost:3000>.
  `pnpm run build` and observe any errors.
* Remove errors.
  * Edit.
    Edit app source file (`layout.tsx`) to remove error involving `Inter`, a
    `next/font/google`.
  * Add config.
    Add a `.vscode/settings.json` file with the property-value pair  
    `"typescript.tsdk": "node_modules/typescript/lib"`  
    to fix a typescript error in tsconfig regarding `resolveJsonModule`.
* (For developer, add remote origin. For example, using an ssh-config
  abbreviation with an ssh-key already generated and integrated into the
  developer's github account,  
  `git remote add origin github:oneforawe/react-next-ts.git`  
  `git push --set-upstream origin main`  
  )
* Reorganize and activate new git configs.
  * Create folder `.config` at root (aka the "config folder").
  * Create file `.gitattributes` in the config folder.
  * Create file `user.gitconfig_template` in the config folder.
  * (For developer, add `user.gitconfig` in the config folder, based on template.)
  * Edit `.gitignore` and move into the config folder.
  * Create file `.gitconfig` at root.
  * Modify the local git config to use the root gitconfig file.  
    `git config --local include.path ../.gitconfig`
* Create new typescript config.  
  `mv .\tsconfig.json .\tsconfig_copy.json`  
  `pnpm exec tsc --init`  
  Combine newly generated tsconfig file with previous copy to yield a much
  more informative commented file.
* Add specification.
  Add to `package.json` an `engines` property to specify appropriate node
  versions.

## Linting

Automatic code-linting is implemented so fixes are applied automatically each
time a file is saved.

Some linting was already partly integrated from the project initialization
(`eslint` and `eslint-config-next`) and with VSCode extensions installed.  Some
other linting must be partly integrated with packages added to the project:

* `pnpm add --save-dev @stylistic/eslint-plugin`
* `pnpm add --save-dev stylelint`
* `pnpm add --save-dev stylelint-config-standard-scss`
* `pnpm add --save-dev --save-exact prettier`

This linting software is further implemented with specifications in the file
`.vscode/settings.json` to indicate which linter/validator/formatter is to be
used with each language and file type.  See those settings for more detail.  For
example, you should see that we use:

* JavaScript/TypeScript linting with [ESLint](https://eslint.org) and
  [Stylistic](https://eslint.style/) (where stylistic is integrated in the
  config file `.config/.eslintrc.json`)
* CSS/SCSS linting with [Stylelint](https://stylelint.io) (validation) and
  [Prettier](https://prettier.io/) (formatting)
* JSON linting with [Prettier](https://prettier.io/)

The app source code showed errors with this linting infrastructure in place, and
some of the errors could be auto-fixed and some required manual fixing.

## Config Folder

Some of the config files have been moved into a custom location -- a config
folder -- to reduce the clutter at the root of the repo.  The config files that
haven't been moved yet into the config folder seem to require default locations
elsewhere, either at the root or in the `.vscode` folder.

* modified: `.gitconfig`  
  Added core properties and an include path

  ```(text)
  [core]
    excludesfile = ./.config/.gitignore
    attributesfile = ./.config/.gitattributes
  [include]
    path = ./.config/user.gitconfig
  ```

  to place three files into the config folder: a git excludes/ignore file, a git
  attributes file, and an optional git user config file (for contributing
  developers).  Another file `user.gitconfig_template` is placed in the config
  folder for reference.
* modified: `package.json`  
  Added an `eslintConfig` property with an `extends` property value of
  `.config/.eslintrc.json` to move the eslint config into the config folder.  
  Added a `stylelint` property with an `extends` property value of
  `.config/.stylelintrc.json` to move the stylelint config into the config
  folder.

## App

The code in the `app` folder was developed from the starting point provided by
create-next-app (the first initializing command) to its current state as the
above steps were taken to hone the project.

## Doc

Continually wrote and revised the documentation.
