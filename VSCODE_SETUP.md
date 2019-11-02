# Setting up VSCode for linting and prettier auto formatting

This is common for all types of projects and linting setup:

First at the root directory of your project, add a `.vscode` folder and inside it add a `settings.json` file.

And add this content to the settings file.

```bash
{
  "eslint.workingDirectories": [
    { "directory": "./", "changeProcessCWD": true }
  ],
  "git.ignoreLimitWarning": true,
  "prettier.singleQuote": false,
  "prettier.bracketSpacing": true,
  "prettier.jsxBracketSameLine": true,
  "prettier.trailingComma": "all"
}
```

Make sure you added the correct directory where your `.eslintrc.json` file exists. Example if your `.eslintrc.json` file is in `client` directory, you should update the working directories config like this:

```bash
"eslint.workingDirectories": [
  { "directory": "./client", "changeProcessCWD": true }
]
```
