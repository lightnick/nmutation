# nmutation
An easy to use plugin that monitors/observes the insertion and deletion of children in a parent element. 
Great for monitoring the size of a container. 

*This plugin uses [MutationObserver API](https://developer.mozilla.org/en/docs/Web/API/MutationObserver) to monitor changes in a DOM*

*Supported browsers*

| Chrome        | Firefox (Gecko) | Internet Explorer  | Opera | Safari 	 |
| ------------- |:---------------:| ------------------:| -----:| -----------:|
| 18 -webkit    | 14 (14) 		  | 11     			   | 15    |  6.0 -webkit|
| 26            |			 	  |                    |       |             |

## Installation
```javascript
  <script src="nmutation.js"></script>
```
## How to use
```javascript
  nmutation.init(target, callback(parent, added, removed));
```
  **target** can be a string or an array: i.e `'.container'` or `['.container', '.your-container']`
  
  **callback** is a function
  * *parent* is the affected or the parent DOM
  * *added* added to parent DOM - default = [ ] empty array
  * *removed* removed from parent DOM - default = [ ] empty array

## Example usage
```javascript
    nmutation.init('div.first', function(parent, added, removed) {
			//Do something awesome...
	});
```
**or**
```javascript
    nmutation.init(['div.first', 'div.second'], function(parent, added, removed) {
			//Do something awesome...
	});
```
Demo http://lightnick.github.io/nmutation/demo.html
