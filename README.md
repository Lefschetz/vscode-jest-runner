# vscode-jest-runner

Looking for collaborators to help me maintain the project. Please contact me at tristanteufel@gmail.com

## Comparison with [vscode-jest](https://github.com/jest-community/vscode-jest)

[vscode-jest-runner](https://github.com/firsttris/vscode-jest-runner) is focused on running or debugging a specific test or test-suite, while [vscode-jest](https://github.com/jest-community/vscode-jest) is running your current test-suite everytime you change it.

## Features

Simple way to run or debug a specific test
_As it is possible in IntelliJ / Webstorm_

Run & Debug your Jest Tests from

- CodeLens

## Supports

- yarn & vscode workspaces (monorepo)
- yarn 2 pnp
- auto detect showUI
- go into workspace before run test(e.g., cd src/app, before run yarn rc-jest ...), you need that when runs into with `require.context`
- run in external terminal

![Extension Example](https://github.com/firsttris/vscode-jest/raw/master/public/vscode-jest.gif)

Check that debugger works:
![image](https://user-images.githubusercontent.com/1709260/120468727-d542ae00-c3a1-11eb-85ac-986c35ac167f.png)

## Extension Settings

.vscode/settings.json

```json
{
  "jestrunner.codeLens": ["run", "watch", "debug"],
  "jestrunner.changeDirectoryToWorkspaceRoot": true,
  "jestrunner.jestCommand": "yarn rc-jest",
  "jestrunner.runOptions": ["--silent", "--colors"],
  "jestrunner.watchOptions": ["--watchPathIgnorePatterns=allure-results"],
  "jestrunner.debugOptions": {
    "program": "",
    "runtimeExecutable": "yarn",
    "runtimeArgs": ["rc-jest"],
    "smartStep": true,
    "skipFiles": ["**/.yarn/**/*.js", "<node_internals>/**/*.js"]
  }
  // "jestrunner.runInExternalNativeTerminal": true, (If you want to run tests in external terminal)
}
```

Note: Please install debug-jest firstly

```
npm_config_registry=https://nexus.int.rclabenv.com/nexus/content/groups/npm-all yarn global add @debug-rtl/debug-jest

```

Note: To open external terminal, please install iterm2 and `yarn global add ttab`

## install

extension -> ... -> install from VSIX -> chose vscode-jest-runner-0.4.60.vsix
