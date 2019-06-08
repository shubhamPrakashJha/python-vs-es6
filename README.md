Python vs ES6
1. General
Function	Python	JavaScript
print	print(x)	console.log(x)
variable	my_var = 1	let myVar = 1
const myVar = 1
Variable Destructuring	x, y, z = 1, 2, 3	[a, b] = [1, 2]
[a, b, ...c] = [1,2,3,4,5]
Assignment Operators	x += 1	x++
Naming Convention	my_var	myVar
Types	int float bool string	number boolean string null undefined object symbol
Type Finding	type(x)	typeof x
typeof(x)
Type Casting	int(4.7)/float(4)/str(4)	Number("3.14")/String(false)/x.toString()
Boolean	False/True	false/true
lambda/arrow Func	add = lambda x: x+10	const max = x => x+10
Null Value	None	null NaN undefined
Comment	#	//
length	len("abc")	"abc".length
(x+y).length
Checking Equality	==	``
Checking Identity	is	``
3. Data Structure
Mutable: Object can be modified after its creation

Immutable: to change this string, you will need to create a completely new string.
                M
  `Sets` `dict` | `List`
U-------------------------------------O
                | `String` `tuple`
                I
Ordered: whether the position of an element in the object can be used to access the element
Mutable & Ordered: List,

Immutable & Ordered: String, tuple

Immutable & UnOrdered: ``,

Mutable & UnOrdered: Sets,

Function	Python	JavaScript
String	"Hello, World"	`sdsd`
List	list_of_random_things = [1, 3.4, 'a string', True]	var mixedData = ["abcd", 1, true, undefined, null, "all the things"];
Tuples	location = (13.4125, 103.866667)	``
Sets	unique_nums = set([1,2,1,3,2])	const unique_nums = new Set([1,2,1,3,2])
Dictionaries	VINIX = {'C': [0.74, -6.51], 'MA': [0.78, 34.77]}	``
``	``
3. Strings
Function	Python	JavaScript
length	len("abc")	"abc".length
(x+y).length
String Casting	str(4)	String(false) x.toString()
Upper Case	"shubham prakash".upper()	"shubham prakash".toUpperCase()
Template String	"Does your {} {}?".format("dog", "bite")	`Does your ${"dog"} ${"bite"}?`
"Does your {1} {0}?".format( "bite", "dog")	
Title Case	"shubham prakash".title()	``
Check Case	"abc".isupper()	``
count pattern	"One fish, two fish".count('fish')	``
find First Occurance	my_string.find('word')	``
find Last Occurance	my_string.rfind('word')	``
Split	"The cow jumped over the moon.".split()	"The cow jumped over the moon.".split(' ')
"The cow jumped over the moon.".split(' ', 3)	"The cow jumped over the moon.".split(' ', 3);
# ['The', 'cow', 'jumped', 'over the moon.']	//["The", "cow", "jumped"]
check substring in string	'this' in 'this is a string' # True	'this is a string'.includes('this') // true
check non-existence of item in List	isa' not in 'this is a string' # True	``
4. List
Function	Python	JavaScript
Random List	list_of_random_things = [1, 3.4, 'a string', True]	const mixedData = ["abcd", 1, true, undefined, null, "all the things"];
Length	len(list_of_random_things)	mixedData.length
maximum	max([1,3,2,4])	``
minimum	min([1,3,2,4])	``
sort	sorted([1,3,2,4])	[1,3,2,4].sort()
join	"-".join(["García", "O'Kelly"])	["García", "O'Kelly"].join('-')
push	letters = ['a', 'b', 'c', 'd']	const letters = ['a', 'b', 'c', 'd']
letters.append('z')	letters.push('z')
# ['a', 'b', 'c', 'd', 'z']	// ["a", "b", "c", "d", "z"]
pop	letters.pop()	letters.pop()
First Item	list_of_random_things[0]	mixedData[0]
Last Item	list_of_random_things[-1]	mixedData[mixedData.length -1]
Slice & Dice	list_of_random_things[1:2] # 3.4	mixedData.slice(1,2) // [1]
list_of_random_things[1:] # [3.4, 'a string', True]	mixedData.slice(1,) // [1, true, undefined, null, "all the things"]
list_of_random_things[:2] # [1, 3.4]	mixedData.slice(0,2) //  ["abcd", 1]
check existence of item in list	"a string" in list_of_random_things # True	mixedData.includes('abcd') // true
check non-existence of item in List	5 not in [1, 2, 3, 4, 6] # True	``
``	``
5. Tuple
Function	Python	JavaScript
Tuple	location = (13.4125, 103.866667)	``
length, width, height = 52, 40, 100	``
dimensions = 52, 40, 100	``
Tuple Unpacking	length, width, height = dimensions	``
``	``
``	``
5. Sets
Function	Python	JavaScript
Sets	fruit = set()	const fruit = new Set();
fruit = {"apple", "banana", "orange", "grapefruit"}	const fruit = new Set(["apple", "banana", "orange", "grapefruit"])
Remove duplicates	numbers = [1, 2, 6, 3, 1, 1, 6]	const numbers = [1, 2, 6, 3, 1, 1, 6]
unique_nums = set(numbers)	unique_nums = new Set(numbers)
# {1, 2, 3, 6}	// {1, 2, 6, 3}
check for element	"watermelon" in fruit	fruit.has("watermelon")
add an element	fruit.add("watermelon")	fruit.add("watermelon")
remove an element	fruit.remove("apple") //if present	fruit.delete('apple') //true
fruit.discard("apple") //if not sure	
remove a random element	fruit.pop() # 'apple'(random)	
Union	``	``
intersection	``	``
difference	``	``
clear Set	fruit.clear()	fruit.clear()
length of set	len(fruit)	fruit.size
5. Dictionaries/Object
Function	Python	JavaScript
create dictionary	elements = dict()	const elements = new Object();
elements = {}	const elements = {};
elements = {"hydrogen": 1, "helium": 2, "carbon": 6}	const elements = {"hydrogen": 1, "helium": 2, "carbon": 6};
Check Keys in dict	"carbon" in elements	"carbon" in elements
elements.hasOwnProperty('carbon')
pull values from keys	elements["helium"] # 2 elements["kryptonite"] # KeyError	elements["helium"] # 2 elements["kryptonite"] # undefined
elements.helium # 2
pull values from key or return (None/user defined msg)	elements.get('kryptonite', 'There\'s no such element!')	``
sort values by keys		``
add values to the dictionary	``	``
``	``
5. Compound Data Structures
Function
i. create Coumpound

# PYTHON
elements = {"hydrogen": {"number": 1,
                         "weight": 1.00794,
                         "symbol": "H"},
              "helium": {"number": 2,
                         "weight": 4.002602,
                         "symbol": "He"}}
// ES6
const elements = {"hydrogen": {"number": 1,
                         "weight": 1.00794,
                         "symbol": "H"},
              "helium": {"number": 2,
                         "weight": 4.002602,
                         "symbol": "He"}}
ii. access Element

# PYTHON
hydrogen_weight = elements["hydrogen"]["weight"]  # get hydrogen's weight
// ES6
hydrogen_weight = elements["hydrogen"]["weight"]
hydrogen_weight = elements.hydrogen.weight  
// get hydrogen's weight
iii. add a new key to the dictionary

# PYTHON
oxygen = {"number":8,"weight":15.999,"symbol":"O"}  # create a new oxygen dictionary 
elements["oxygen"] = oxygen  # assign 'oxygen' as a key to the elements dictionary
print('elements = ', elements)
# elements =  {"hydrogen": {"number": 1,
#                           "weight": 1.00794,
#                           "symbol": 'H'},
#                "helium": {"number": 2,
#                           "weight": 4.002602,
#                           "symbol": "He"}, 
#                "oxygen": {"number": 8, 
#                           "weight": 15.999, 
#                           "symbol": "O"}}
 
// ES6
const oxygen = {"number":8,"weight":15.999,"symbol":"O"}  // create a new oxygen dictionary 
elements["oxygen"] = oxygen //or
elements.oxygen = oxygen  // assign 'oxygen' as a key to the elements dictionary
console.log('elements = ', elements)
// elements =  {"hydrogen": {"number": 1,
//                           "weight": 1.00794,
//                           "symbol": 'H'},
//                "helium": {"number": 2,
//                           "weight": 4.002602,
//                           "symbol": "He"}, 
//                "oxygen": {"number": 8, 
//                           "weight": 15.999, 
//                           "symbol": "O"}}
 
