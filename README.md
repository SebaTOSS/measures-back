<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo_text.svg" width="320" alt="Nest Logo" /></a>
</p>

## Description
<p>This is an example of how to configure and use <a href="https://nestjs.org" target="blank">NestJS</a> framework.</p>

## Installation
<p>Download and install these tools</p>
<ul>
  <li>
    <a href="https://git-scm.com" target="blank">GIT</a>
  </li>
  <li>
    <a href="https://www.sourcetreeapp.com" target="blank">SourceTree</a> (only for windows)
  </li>
  <li>
    <a href="http://nodejs.org" target="blank">NodeJS</a>
  </li>
  <li>
    <a href="https://www.python.org/" target="blank">Python</a>
  </li>
  <li>
    <a href="https://www.postgresql.org/download" target="blank">PostgreSQL</a>
  </li>
  <li>
    <a href="https://www.pgadmin.org" target="blank">PGAdmin</a>
  </li>
  <li>
    <a href="https://code.visualstudio.com" target="blank">Visual Studio Code</a>
  </li>
</ul>

<p>Then clone this repo locally. Using a shell perform this command inside the folder (where package.json file is located)</p>

```bash
$ npm install
```
<p>Open Visual Studio Code and open the folder with the project. Create a new launch.json file to run the app, click on Run icon and select NodeJS attach process.
Replace the file with this content.</p>

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "node",
            "name": "Tests",
            "request": "launch",
            "args": [
                "--runInBand"
            ],
            "cwd": "${workspaceFolder}",
            "console": "integratedTerminal",
            "internalConsoleOptions": "neverOpen",
            "disableOptimisticBPs": true,
            "program": "${workspaceFolder}/node_modules/jest/bin/jest"
        },
        {
            "type": "node",
            "request": "launch",
            "name": "LOCAL",
            "args": ["${workspaceFolder}/src/main.ts"],
            "restart": true,
            "autoAttachChildProcesses": true,
            "runtimeArgs": ["--nolazy", "-r", "ts-node/register"],
            "sourceMaps": true,
            "stopOnEntry": false,
            "cwd": "${workspaceRoot}",
            "protocol": "inspector",
            "skipFiles": [
                "${workspaceFolder}/node_modules/**/*.js",
                "${workspaceFolder}/lib/**/*.js"
            ],
            "env": {}
        }
    ]
}
```

## Running the app

<p>Click in run icon and select LOCAL setup. On the terminal (inside the IDE) it should appear some logs. Wait until the app is up. Open a web browser and go
<a href="http://localhost:3000" target="_blank">here</a>. It should appear a message as response</p>

## Test

```bash
# unit tests
$ npm run test

# test coverage
$ npm run test:cov
```

## Stay in touch

- Author - [Sebastian](https://github.com/SebaTOSS)

## License

  Nest is [MIT licensed](LICENSE).
