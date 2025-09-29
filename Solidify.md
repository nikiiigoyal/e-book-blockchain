**VERSIN** : Declaration of version to prevent issues with future compiler versions
**CONTRACT** : All functions and variables
**State variables** : These are permanently stored in contract storage. This means they're written to the Ethereum blockchain. Think of them like writing to a DB.
**Unsigned Integers** : uint
The uint data type is an unsigned integer, meaning its value must be non-negative. There's also an int data type for signed integers.

*Note: In Solidity, uint is actually an alias for uint256, a 256-bit unsigned integer. You can declare uints with less bits — uint8, uint16, uint32, etc..*
<!-- pragma solidity >=0.5.0 <0.6.0;.
contract HelloWorld {
uint myUnsignedInteger = 100;
} -->

**structs** : Structs allow you to create more complicated data types that have multiple properties.
**Arrays** : When you want a collection of something, you can use an array. There are two types of arrays in Solidity: fixed arrays and dynamic arrays:
<!-- uint[2] fixedArray;
a dynamic Array - has no fixed size, can keep growing:
uint[] dynamicArray -->

**Public Arrays** : You can declare an array as public, and Solidity will automatically create a getter method for it. The syntax looks like:
<!-- Person[] public people; -->

**Functions** :
<!-- function eatHamburgers(string memory _name, uint _amount) public {

} -->
function named *eatHamburgers* that takes 2 parameters: *a string and a uint*. 
function visibility as public. 
providing instructions about where the *_name variable should be stored- in memory*. This is required for all reference types such as arrays, structs, mappings, and strings.function parameter variable names with an underscore (_) in order to differentiate them from global variables.

What is a reference type you ask?

Well, there are two ways in which you can pass an argument to a Solidity function:
**By value**, which means that the Solidity compiler creates a new copy of the parameter's value and passes it to your function. This allows your function to modify the value without worrying that the value of the initial parameter gets changed.
**By reference**, which means that your function is called with a... reference to the original variable. Thus, if your function changes the value of the variable it receives, the value of the original variable gets changed.

Two types of Functions:

**Public** : functions are public by default. This means anyone (or any other contract) can call your contract's function and execute its code

**Private** :  use the keyword private after the function name. And as with function parameters, it's convention to start private function names with an underscore (_).This means only other functions within our contract will be able to call this function and add to the numbers array.
<!-- function _addToArray(uint _number) private {
  numbers.push(_number);
} -->

**Return** :
To return a value from a function, the declaration looks like this:
<!-- string greeting = "What's up dog";
function sayHello() public returns (string memory) {
  return greeting;
} -->
In Solidity, the function declaration contains *the type of the return value* (in this case string).

**Function Modifiers** :

**view function**, meaning it's only viewing the data but not modifying it:
**Pure** : means you're not even accessing any data in the app.

**keccak256** : 
built in hash function, version of SHA3. 
hash function basically maps an input into a random 256-bit hexadecimal number. A slight change in the input will cause a large change in the hash.
keccak256 expects a single parameter of type *bytes*.

**Typecasting** : convert between data types.
<!-- uint8 a = 5;
uint b = 6;
// throws an error because a * b returns a uint, not uint8:
uint8 c = a * b;
// we have to typecast b as a uint8 to make it work:
uint8 c = a * uint8(b); -->

**Events** : Events are a way for your contract to communicate that something happened on the blockchain to your app front-end, which can be 'listening' for certain events and take action when they happen.

<!-- // declare the event
event IntegersAdded(uint x, uint y, uint result);

function add(uint _x, uint _y) public returns (uint) {
  uint result = _x + _y;
  // fire an event to let the app know the function was called:
  emit IntegersAdded(_x, _y, result);
  return result;
} -->
