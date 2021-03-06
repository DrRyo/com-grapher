# COM Grapher
![COM Grapher](https://user-images.githubusercontent.com/9062624/57970046-64491d00-79b7-11e9-8259-6d960aa5ce89.png)
Simple graph viewer communicates with serial(COM port).

## Getting Started

You can easily start with Download this project ZIP

### Prerequisites

* [Node.js](https://nodejs.org/) 10.15.3 or 12.2.0 *(Any version will be okay, but not sure)*
* [Visual Studio Build Tools](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools) or [Visual Studio 2017 Community](https://visualstudio.microsoft.com/pl/thank-you-downloading-visual-studio/?sku=Community)
* [Python 2.7](https://www.python.org/)

### Build
1. Install [Node.js](https://nodejs.org/) *(Any version will be okay, but not sure)*
   
2. Follow [node-gyp installation](https://github.com/nodejs/node-gyp#installation) and make sure node-gyp is properly configured

3. Install required npm package for build:
```bash
npm install
```

4. Rebuild packages, additionally rebuild serialport with *--update-binary* option:
```bash
npm rebuild
npm rebuild serialport --update-binary
```
   or, you can just run command below
```bash
npm run rebuild
```

5. Rebuild electron:
```bash
./node_modules/.bin/electron-rebuild
```

6. *(Windows only)* To build executable, run this command. This will create **dist** folder with installer and portable:
```bash
npm install -g electron-builder
electron-builder install-app-deps
npm run build:win
```

### Usage
#### Transmit Data Type
* Data in one line, delimited by as you input (\r, \n, \r\n ...)
* Data string should be enclosed with square brackets
* Only numbers(or floats) are allowed
* **25nd data will be recognized by angle** (If you don't want, see below)

For example, following data will accepted and decoded well by program
```
[1, 2, 3, 4, 5, 0.001, 0.002, 0.003, 0.004, 0.005]\n
```
or
```
[1, 2, 3, 4, 5, 0.001, 0.002, 0.003, 0.004, 0.005]\r
```
or
```
[1, 2, 3, 4, 5, 0.001, 0.002, 0.003, 0.004, 0.005]\r\n
```

#### What is Arm, Dumbbell, Encoder, Angle Index?
* It's for my own usage, put **Angle Index** to **maximum value** if you don't want.

## Authors

* **Ryo** - *Whole work*

## License

This project is licensed under the MIT License - see the LICENSE file for details

## Credits
Icons made by [Smashicons](https://www.flaticon.com/authors/smashicons) from [www.flaticon.com](https://www.flaticon.com/) is licensed by [CC 3.0 BY](http://creativecommons.org/licenses/by/3.0/)

## Acknowledgments

* Just lab work :)
