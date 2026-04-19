OR `||` , And `&&`  , Not  `!`
### 1. OR 
_you know how this goes._
**But there's an interesting features in JS:**
1. **Getting the first truthy value from a list of variables or expressions:
    
    - For instance, we have `firstName`, `lastName` and `nickName` variables, all optional (i.e. can be undefined or have falsy values).
    
    - Let’s use OR `||` to choose the one that has the data and show it (or `"Anonymous"` if nothing set):
    ```javascript
    let firstName = "";
    let lastName = "";
    let nickName = "SuperCoder";
    
    let chosen = ( firstName || lastName || nickName || "Anonymous");
	console.log(chosen); // "SuperCoder"
    ```

2. **Short-circuit evaluation.**

	- Another feature of OR `||` operator is the so-called “short-circuit” evaluation.
		
	- It means that `||` processes its arguments until the first **truthy** value is reached from left to right, and then the value is returned immediately, without even touching the other argument.
		
	- The importance of this feature becomes obvious if an operand isn’t just a value, but an expression with a side effect, such as a **variable** **assignment** or a **function** call.
### 2. AND

-  The same **short-circuit evaluation** happens in **AND** but it returns the first falsy operand
### 3. NOT

- `if (!Equal);`  _you know this stuff_
