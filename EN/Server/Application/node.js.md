based on V8 JavaScript engine of Google Chrome, check support on different browsers on [Node Green](https://node.green)

[node.js Project page](https://nodejs.org/en/) [node.js API overview](https://nodejs.org/api/)

[Node.js Releases](https://nodejs.org/en/about/previous-releases#nodejs-releases) two new versions per year, even versions running 30 month

### Missing objects in node.js 
- **Window** `window.alert("Helo World");` will not work
- Document Object Model (DOM)
- Cookies
## Run a JavaScript program with node.js
Most common way by calling a script
```console
node hello.js
```
Running in Interactive mode (REPL Mode - Read Evaluate Print Loop) Tab is helpful
```console
~$ node
Welcome to Node.js v14.17.5.
Type ".help" for more information.
> .load hello.js
console.log("Hello World!");
Hello World"
> .save
> .break
> .exit
```

### Example JavaScript Function in node.js
```js
function ggT(a,b){
	if (a == 0) return b;
	while ( b != 0 ) {
		let temp = a % b;
		a = b;
		b = temp;
	}
return a;
}

function kgV(a, b) {
	if ( a==0 || b==0 ) return 0;
	return (a * b) / ggt(a, b);
}

/* module.exports = kgV; */
exports.ggt = ggT;
exports.kgV = kgV;
```
**File: calct.js** (Modul)
```js
/* const kgV = require("./calc.js"); */
const calc = require("./calc.js");
					 
console.log(calc.kgV(12, 18));
console.log(calc.ggT(35, 10));
```
**File: app.js**
```console
node app.js
```
**Call app.js in node.js**

Create a  webserver with node.js
```js
const http = require('http);

const server = http.creteServer((request, response) => {
		response.statusCode = 200;
		response.setHeader('Content-Type', 'text/html');
		response.end('<html><body><h1>Hello World!</h1></body></html>');			
	  });

server.listen(8080);

process.on('SIGTERM', () => {
		server.close(() => {
			console.log('Webserver shutdown!');
			});
});
```
