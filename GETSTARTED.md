# WebdriverIO-project

### Frameworks
- `WebdriverIO`
- `Mocha`

### Built With
* [Node.js](https://nodejs.org/en/)
* [JQuery](https://jquery.com)
* [Mocha Test runner]()
## Getting Started 

### Prerequisites

- Install Node.js
- Install Java 8 
- Install Allure CLI

### Installation

1. Clone the repo
2. Install packages
   ```bash
   npm install
   ```
3. To run the project you will need to create a `.env` file in the root directoy of the project. Paste the content below inside the file:

```bash
EMAIL=Firstname.lastname@yourdomain.test
PASWORD=Tosca1234!
```

 Enter the correct values for `EMAIL` and `PASSWORD`

----


## Usage

### Run Tests
You can start your test suite by using the `run` command and pointing to a WebdriverIO config file

```bash
npx wdio run ./test/config/wdio.local.conf.js
```

If you like to run specific test files you can add a --spec parameter:
```bash
npx wdio run ./test/config/wdio.local.conf.js --spec login.spec.js
```
or 
```bash
npm run local
```


## Tips & Tricks

### `Running in Debug Mode`

If you want to debug your tests with breakpoints in latest VSCode, you have to install and enable the nightly verison of the JavaScript Debugger. ([JavaScript Debugger (Nightly)](https://marketplace.visualstudio.com/items?itemName=ms-vscode.js-debug-nightly)).

To run all or selected spec file(s). Debug configuration(s) have to be added to .vscode/launch.json, to debug selected spec add the following config:
```json
 {
 "launch": {
		"version": "0.2.0",
		"configurations": [
        {
            "name": "wdio-test",
            "type": "node",
            "request": "launch",
            "args": [
                "./class-content/01-webdriverio/src/test/config/wdio.local.conf.js",
                "--spec",
                "${file}"
            ],
            "cwd": "${workspaceFolder}",
            "autoAttachChildProcesses": true,
            "program": "${workspaceRoot}/class-content/01-webdriverio/src/node_modules/@wdio/cli/bin/wdio.js",
            "console": "integratedTerminal"
        }
    ]
	}
 }
```




