- [๐ From.js](#-fromjs)
  - [๐ฆ Installation](#-installation)
    - [๐ง How to use](#-how-to-use)
      - [โจ Importing](#-importing)
          - [Common Js](#common-js)
          - [Js Modules](#js-modules)
      - [๐ฅ Install module](#-install-module)
      - [๐ Removing module](#-removing-module)
      - [๐ Importing module](#-importing-module)
      - [๐งถ Updating a module](#-updating-a-module)
      - [๐ค Checking a module version](#-checking-a-module-version)
      - [๐ค Checking if a module is installed](#-checking-if-a-module-is-installed)
    - [๐ญ Events](#-events)
      - [install](#install)
      - [remove](#remove)
      - [update](#update)
  - [๐ License](#-license)

# ๐ From.js
An easy and fast importer of global modules

## ๐ฆ Installation

**YARN**
```bash
yarn add from.js
```

**NPM**
```bash
npm install from.js
```

### ๐ง How to use

#### โจ Importing
###### Common Js
```js
const fromJs = require("from-module");
```

###### Js Modules
```js
import fromJs from "from-module";
```

#### ๐ฅ Install module
```js
// False to install with npm
// True to install with yarn

fromJs.i("moduleName", false /* default */, (mods) => `Installed ${mods[0]}!`)
```

#### ๐ Removing module
```js
fromJs.r("moduleName", (mods) => `Removed ${mods[0]}!`)
```

#### ๐ Importing module
```js
fromJs("moduleName", (mod) => {
    // Your code here
})
```

#### ๐งถ Updating a module
```js
// False to update with npm
// True to update with yarn

fromJs.update("moduleName", false /* default */)
```

#### ๐ค Checking a module version
```js
fromJs.version("moduleName") // If the module is not in package.json it will return undefined
```

#### ๐ค Checking if a module is installed
```js
if (fromJs.has("moduleName")) console.log("The module is installed")
else console.log("The module is not installed")
```

### ๐ญ Events
#### install
```js
fromJs.on("install", (std, modules) => {
  // Your code here
})
```

#### remove
```js
fromJs.on("remove", (std, modules) => {
  // Your code here
})
```

#### update
```js
fromJs.on("update", (std, modules) => {
  // Your code here
})
```

## ๐ License
MIT License

Copyright (c) 2021 Brian Rhudy

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
