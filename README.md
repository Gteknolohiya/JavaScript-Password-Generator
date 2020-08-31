README v1.0 / 31 AUGUST 2020

# JavaScript-Password-Generator

## Introduction

JavaScript Password Generator generates random uppercase and lowercase letters, numbers and symbols based on password length you want.

## Usage

First, you need to put the length of password you want. Next, modify the password settings you want(e.g, Uncheck lowercase if you don't want a lowercase letter.). Lastly, click the "GENERATE PASSWORD" button to generate random password. Just click the copy icon if you want to copy it.

## How to create it?

You need to generate a random uppercase, lowercase, numbers and symbols to create it. First create function that generate lowercase, uppercase, numbers, and symbols. You need to use Math.random() to produce random decimal numbers. To make it whole number, put it inside of Math.floor(). I multiply 26 because that is the total numbers of alphabet. Then I add 97 because that is the start of lowercase letter. Do the same with the others. In symbol part, I create variable of symbols('!@$%^&*(){}[]=<>/,.') and return it with Math.floor() and Math.random() plus 19(no. of symbols). After that, I put the functions into an object called randomFunc. Next, I create the DOM elements. Then, I create the event listener for "Generate Password". Create length variable to get the value of password length. The value is a string, so convert it into number. To convert it, add "+" before the variable(e.g, +lengthEl.value;). To verify if the pw setting is checked, create a variable "hasLower, hasUpper, hasSymbol, hasNumber". Use the DOM element in it and put .checked to verify if it is true or false. After that, pass it in resultEl.innerText = generatePassword(). Next, create function generatePassword() and pass in upper, lower, number, symbol, length. Inside this function, the first thing you need to do is to initialize pw variable. Then create typesCount variable to know to number of types. Next, create typesArr variable to put it inside an array. You need to put curly braces in every parameter to make it like "symbol: true". Filter what is false by putting .filter to the array.(e.g,  const typesArr = [{upper}, {lower}, {number}, {symbol}].filter(item => Object.values(item)[0]). Check if there's non-checked. If there's no check, it won't proceed.(e.g,    if(typesCount === 0) {return '';}). Loop typeArr array. Slice off whatever the length is in this case to avoid the default four values even their is 0 length.(e.g, const finalPassword = generatedPassword.slice(0, length);). Create a finalPassword variable and return it. You need to create a functionality that copy the generated pw to clipboard. Create event listener for clipboardEl. to copy it from clipboard, textarea.value = password; , document.body.appendChild(textarea); , textarea.select(); , document.execCommand('copy'); , textarea.remove(); , alert('Password copied to clipboard!');. Also, create     if(!password) {return;}; to return nothing if there is no value/text.

## Important Notes

- To generate random decimal number, use Math.random().
- To make it whole number, use Math.floor().
- To convert string to number, add "+" before the variable(e.g, +lengthEl.value;).
- To check a checkbox if the value is true or false, use .checked at the end of the DOM element.
- To remove existing value, use .slice.(e.g, const finalPassword = generatedPassword.slice(0, length);).
- to create a functionality that copy the generated pw to clipboard, textarea.value = password; , document.body.appendChild(textarea); , textarea.select(); ,   document.execCommand('copy'); , textarea.remove(); , alert('Password copied to clipboard!');.
 
## Contributing

To contribute in this project, just contact me on my fb page Gteknolohiya or email me at gteknolohiya@gmail.com.

## Help

If you have some questions, just message me on my fb page.

### Requirements

There's no specific requirements.

### Installation

Go to https://gteknolohiya.github.io/Javascript-Password-Generator

### Configuration

N/A

## Credits

Credits to Traversy Media for the tutorial of this app.

## Contact

FB page: https://facebook.com/gteknolohiya
Email: gteknolohiya@gmail.com

## License

N/A
