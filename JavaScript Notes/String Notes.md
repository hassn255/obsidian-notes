# **Strings**
**Note**
- To change a string number to a number you do +'1' and it changes to 1 
Example:

```javascript
let a = "1";
let b = 0;
switch(+a){                   // '+' here makes a an actual number
	case b+1:
		...
		break;
	
	default:
		...
		break;
}
```

![[Pasted image 20251128175005.png]]
-  You can also do `text[Number]`but 
![[Pasted image 20251128181143.png]]


### **Extracting a string**

**There are 3 methods to Extract a string** : `Slice , substring, substr`

- `let text = BananaBreadButter` 
	1.  `slice(_start_, _end_)` 
		-  If you write slice(6) it will slice until it reaches the **7th** letter, so from Bread to the end **n + 1**
		-  if you write slice(6,12) it will slice from **7 to 12**
		-  if you write slice(-5) it will slice from the end to the 5th letter and take the 5th from the right and return it
		- `let part = text.slice(-12, -6);` 

	2. `substring(_start_, _end_)`
		-  it is similar to slice but it treats lower than 0 as 0
		- so `let part = text.substring(-10, 2);` just gives **Ba** and anything after the end of the string just returns the whole string 
		- `let part = text.substring(-10, 200);` returns **BananaBreadButter**

	3. `substr(_start_, _length_)` it is **deprecated** in the latest JS releases
### **Converting to Upper and Lower Case**

A string is converted to upper case with `toUpperCase()`:

A string is converted to lower case with `toLowerCase()`:

### **isWellFormed**

```javascript
let text = "Hello world \uD800";
let part = text.substring(-10, 202);
console.log(text);
let wellFormed = text.toWellFormed();
console.log(wellFormed);

OUTPUT:
Hello world � <- THIS IS NOT LETTERS

Hello world � <- toWellFormed() made this letters
```


### **JavaScript String trim()**
The trim() method removes whitespace from both sides of a string:

Example
```javascript
let text1 = "      Hello World!      ";
let text2 = text1.trim(); // "Hello World!"
JavaScript String trimStart() // "Hello World!      "
JavaScript String trimEnd() // "      Hello World!"

```

### **String Padding**

The `padStart()` method is a string method.
To pad a number, convert the number to a string first.

```javascript
let number = 5;  
let text = numb.toString();  
let padded = text.padStart(4,"0");  // the number = 0005 notice that there are 4 - 1 zeros
let paddedEnd = text.padEnd(4,"0"); // "5000"
```

### **String Repeat**
`repeat(n)` to repeat the string n times

```javascript
let text = "Hazem";
let repeat = text.repeat(3) // repeat = "HazemHazemHazem"
```

### **## Replacing String Content

The `replace()` method replaces a specified value with another value in a string:
```javascript
let text = "Please visit Microsoft!";  
let newText = text.replace("Microsoft", "BHS Academy");**
// newText = "Please visit BHS Academy!"
```
- This replaces **ONLY** the first match
- to make the replace case insensitive, use a **regular expression** with an `/i` flag (insensitive):
```javascript
let text = "Please visit Microsoft!";  
let newText = text.replace(/MICROSOFT/i, "W3Schools");
```
- To replace all the matches do **/g** or use `replaceAll()`
 ###

### **JavaScript String split()**

A string can be converted to an array with the `split()` method:
```javascript
text.split(",")    // Split on commas  
text.split(" ")    // Split on spaces  
text.split("|")    // Split on pipe
text.spllit("")    // Split every char
```
If the separator is not found, the returned array will contain the whole string in index [0].

If the separator is "", the returned array will be an array of single characters:
so 
```javascript
let text = "   Hazem,Magdy,Mahmoud,Hamdy   ";

let stringArray = text.trim().split(",");

for (let index = 0; index < stringArray.length; index++) {

const thisString = stringArray[index];

console.log(thisString);         // Hazem/nMagdy/nMahmoud/nHamdy
			                        0       1       2        3

}
```