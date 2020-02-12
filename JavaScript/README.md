# Javascript Code Book

## Naming Variables

*Always use semantic variables*.

Only use _ underscores for private variables.

Only user *const* or *let*.



## Objects

### YES
`const newObject = {
	firstName: 'Tatyana',
	lastName: 'Fazlalizadeh',
}`

### BAD
  `const newObject = { firstName: 'Tatyana', lastName: 'Fazlalizadeh', }`

### BAD
`const newObject = { firstName: 'Tatyana',
	lastName: 'Fazlalizadeh', }`

## Arrays

### GOOD
`const myArray = [
	'Tatyana',
	'Fazlalizadeh',
]`

### BAD
`const myArray = [ 'Tatyana', 'Fazlalizadeh', ]`

### BAD
`const myArray = [ 'Tatyana',
	'Fazlalizadeh', ]`


If, then, else
`let someVar = 'Something'`

### GOOD
`if (someVar) {
	callSomeFunc(someVar)
} else {
	doSomethingElse()
}`

### BAD
`if (someVar) { callSomeFunc(someVar) } else { doSomethingElse() }`

### BAD
`if (someVar) {
 callSomeFunc(someVar)
}
else {
 doSomethingElse()
}`

### GOOD
`if ('parameter' === someVar) {
	callSomeFunc(someVar)
} else
if ('otherParameter' === someVar) {
	doSomethingElse()
}`

### GOOD - spacing between parentheses is acceptable
`if ( 'parameter' === someVar ) {
	callSomeFunc( someVar )
} else
if ( 'otherParameter' === someVar ) {
	doSomethingElse()
}`

### BAD
`if ('parameter' === someVar)
{
	callSomeFunc(someVar)
}
else if ('otherParameter' === someVar)
{
	doSomethingElse()
}`

### BAD
`if ('parameter' === someVar)
{
	callSomeFunc(someVar)
} else if ('otherParameter' === someVar)
{
	doSomethingElse()
}`

### BAD
`if (
    firstCondition() &&
    secondCondition() &&
    thirdCondition()
) {
    doStuff();
}`

### BAD
`if (
    someThing
) {
    doStuff();
}`

### GOOD
`(someVar) ? 'we fit in' : 'one line'`

### GOOD
`(someVar)
	? 'parameter is'
	: 'even better'
`
### BAD
`(someVar) ?
	'parameter is' :
	'not good'
`
### BAD
`(someVar)
? 'parameter is'
: 'not good'
`
### GOOD
`(someVar) && doSomething()`

### GOOD
`someVar
	&& someOtheVar
	&& doSomething()
`
### BAD
`someVar &&
someOtheVar &&
doSomething()
`
### BAD
`someVar &&
	someOtheVar &&
	doSomething()
`
### BAD
`someVar && someOtheVar && doSomething()`

##Left-Hand Operators

### GOOD
`if (0 < someArray.length) {
	// do something
}`

### GOOD
`if ('' !== someString) {
	// do something
}`

### GOOD
`if ('function' !== typeof funcToTest) {
	// do something
}`

### BAD
`if (someArray.length > 0) {
	// do something
}`

### BAD
`if (someString !== '') {
	// do something
}
`
### BAD
`if (typeof funcToTest !== 'function') {
	// do something
}
for loop
### GOOD - loop through an array
let i;
for (i = 0; i < someArray.length; i++) {
	// do something with someArray[i]
}`

### BAD
`for (i = 0; i < someArray.length; i++) {
	// do something with someArray[i]
}`

### BAD
`for (i = 0; i < someArray.length; i++)
{
	// do something with someArray[i]
}`

### GOOD - loop through an object
`for (let i in someObject) {
	if (someObject.hasOwnProperty(i)) {
		// do something with someArray[i]
	}
}`

### GOOD
`for (let i = 0; i < Object.keys(someObject).length; i++) {
	// do something with someObject[i]
}`

### BAD
`for (let i in someObject)
{
	if (someObject.hasOwnProperty(i))
	{
		// do something with someArray[i]
	}
}`

### BAD
`for (let i in someObject) {
	// do something with someArray[i]
}`

### BAD
`for (let i in someObject) {
	if (someObject[i]) {
		// do something with someArray[i]
	}
}`

## try, catch

### GOOD
`try {
    // Expressions
} catch ( e ) {
    // Expressions
}`

### BAD
`try
{
    // Expressions
} catch ( e )
{
    // Expressions
}`

### BAD
`try {
    // Expressions
}
catch ( e ) {
    // Expressions
}`

## ABSOLUTELY WRONG!
`try {
    // Expressions
}`
