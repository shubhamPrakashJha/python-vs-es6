# Python vs ES6

## 1. __General__

| Function | Python | JavaScript |
| --- | ------ | ---- |
| print | `print(x)` | `console.log(x)` |
| Take Input | `const x = input()` | `const x = prompt()` |
| | `x = int(input())` | `const x = Number(prompt())` |
| |  | `const x = Number(window.prompt())` |
| | `z = int(input("Give Input:"))` | `const z = Number(window.prompt("Give Input:"))` |
| variable | `my_var = 1`| `let myVar = 1` |
|  | | `const myVar = 1` |
| Variable Destructuring | `x, y, z = 1, 2, 3` | `[a, b] = [1, 2]` |
|  |  | `[a, b, ...c] = [1,2,3,4,5]` |
| Assignment Operators | ` x += 1` | `x++` |
| Naming Convention  | `my_var` | `myVar` |
| Types | `int` `float` `bool` `string`| `number` `boolean` `string` `null` `undefined` `object` `symbol`|
| Type Finding | `type(x)` | `typeof x` |
| | | `typeof(x)` </br>`//only for above mentioned types` |
| | | `Array.isArray(some_var)` </br>`//to check for array` |
| Type Casting | `int(4.7)/float(4)/str(4)` | `Number("3.14")/String(false)/x.toString()`|
| Boolean | `False/True` | `false/true` |
| Null Value | `None`| `null` `NaN` `undefined`|
| Comment | `#`| `//` |
| length | `len("abc")`| `"abc".length` |
| | | `(x+y).length` |
| Checking Equality | `==`| `==` |
| Checking Equality and Type | `==`| `===` |
| Checking Identity | `is`| `` |
| lambda/arrow Func | `add = lambda x: x+10` | `const add = x => x+10` |
| lambda/arrow Func |  | `const add = (x, y) => x+y` |
| map() | `list(map(func, arr))` | `arr.map(func)` |
|  | `list(map(lambda x: x*2 , [1,2,3]))` </br>`# [2, 4, 6]` | `[1,2,3].map(x => x*2)` </br>`// [2, 4, 6]` |
| filter | `list(filter(func, arr))` | `arr.filter(func)` |
|  | `list(filter(lambda x: (x%2 != 0) , [1,2,3]))` </br>`# [1, 3]` | `[1,2,3].filter(x => (x%2 != 0))`</br> `// [1, 3]` |
| Reduce | `from functools import reduce` | ```arr.reduce( (accumulator, currentValue, currentIndex, array) => accumulator + currentValue);``` |
|  | ```reduce((lambda accumulator, currentValue: accumulator + currentValue), li)``` |  |
|  | `from functools import reduce` | `` |
|  | `reduce((lambda x, y: x + y), [1,2,3]) ` | `[1,2,3].reduce((x,y) => x+y)` |
| And | `and` | `&&` |
| Or | `or` | `||` |
| Not | `not` | `!` |

## 2. __Data Structure__

```def
Mutable: Object can be modified after its creation

Immutable: to change this string, you will need to create a completely new string.
                M
  `Sets` `dict` | `List`
U-------------------------------------O
                | `String` `tuple`
                I
Ordered: whether the position of an element in the object can be used to access the element
```

> _Mutable & Ordered_: `List`,

> _Immutable & Ordered_: `String`, `tuple`

> _Immutable & UnOrdered_: ``, 

> _Mutable & UnOrdered_: `Sets`, `dictionary/Object`



| Function | Python | JavaScript |
| --- | ------ | ---- |
| String | `"Hello, World"` | ``` `sdsd` ``` |
| List | `list_of_random_things = [1, 3.4, 'a string', True]` | `var mixedData = ["abcd", 1, true, undefined, null, "all the things"];` |
| Tuples | `location = (13.4125, 103.866667)` | `` |
| Sets | `unique_nums = set([1,2,1,3,2])` | `const unique_nums = new Set([1,2,1,3,2])` |
| Dictionaries | `VINIX = {'C': [0.74, -6.51],  'MA': [0.78, 34.77]}` | `const elements = {"hydrogen": 1, "helium": 2, "carbon": 6};` |
|  | `` | `` |


## 2.1. __Strings__

| Function | Python | JavaScript |
| --- | ------ | ---- |
| length | `len("abc")`| `"abc".length` |
| | | `(x+y).length` |
| String Casting | `str(4)` | `String(false)` `x.toString()`|
| Upper Case | `"shubham prakash".upper()`| `"shubham prakash".toUpperCase()` |
| Template String| `"Does your {} {}?".format("dog", "bite")`| ``` `Does your ${"dog"} ${"bite"}?` ```|
| | `"Does your {1} {0}?".format( "bite", "dog")` | |
| Title Case | `"shubham prakash".title()`| ```"shubham prakash".split(' ').map(word => `${word[0].toUpperCase()}${word.slice(1,)}`).join(' ')``` |
|  | ```" ".join(list(map(lambda word: '{}{}'.format(word[0].upper(), word[1:]), "shubham prakash".split())))``` |  |
| Check Case | `"abc".isupper()`| `"shubham prakash" === "Shubham Prakash".toLocaleLowerCase()` |
| count pattern | `"One fish, two fish".count('fish')`| `"One fish, two fish".match(/fish/gi).length` |
| find First Occurance| `my_string.find('word')`| `"One fish, two fish".match('fish').index` |
| find Last Occurance| `my_string.rfind('word')`| `"One fish, two fish".lastIndexOf('fish')` |
| Split | `"The cow jumped over the moon.".split()` | `"The cow jumped over the moon.".split(/[ ]+/)` |
| | `"The cow jumped over the moon.".split(' ', 3)` | `"The cow jumped over the moon.".split(' ', 3);` |
| | </br>`# ['The', 'cow', 'jumped', 'over the moon.']` | </br>`//["The", "cow", "jumped"]` |
| check substring in string | `'this' in 'this is a string'` </br>`# True` | `'this is a string'.includes('this')` </br>`// true` |
| check non-existence of item in List | `isa' not in 'this is a string'` </br>`# True` | `!'this is a string'.includes('notExist')` </br>`// true` |


## 2.2. __List/Array__
| Function | Python | JavaScript |
| --- | ------ | ---- |
| Random List | `list_of_random_things = [1, 3.4, 'a string', True]` | `const mixedData = ["abcd", 1, true, undefined, null, "all the things"];` |
| Length | `len(list_of_random_things)` | `mixedData.length` |
| maximum | `max([1,3,2,4])` | `Math.min( ...arr )` |
| minimum | `min([1,3,2,4])` | `Math.min( ...arr )` |
| sort | `sorted([1,3,2,4])` | `[1,3,2,4].sort()` |
| join | `"-".join(["García", "O'Kelly"])` | `["García", "O'Kelly"].join('-')` |
| push | `letters = ['a', 'b', 'c', 'd']`  | `const letters = ['a', 'b', 'c', 'd']` |
| | `letters.append('z')`| `letters.push('z')` |
|  | `# ['a', 'b', 'c', 'd', 'z']` | `// ["a", "b", "c", "d", "z"]` |
| pop | `letters.pop()` | `letters.pop()` |
| First Item | `list_of_random_things[0]` | `mixedData[0]` |
| Last Item | `list_of_random_things[-1]` | `mixedData[mixedData.length -1]` |
| Slice & Dice | `list_of_random_things[1:2]` </br>`# 3.4` | `mixedData.slice(1,2)` </br>`// [1]` |
|  | `list_of_random_things[1:]` </br>`# [3.4, 'a string', True]` | `mixedData.slice(1,)` </br>`// [1, true, undefined, null, "all the things"]` |
|  | `list_of_random_things[:2]` </br>`# [1, 3.4]` | `mixedData.slice(0,2)` </br>`//  ["abcd", 1]` |
| check existence of item in list | `"a string" in list_of_random_things` </br>`# True` | `mixedData.includes('abcd')` </br>`// true` |
| check non-existence of item in List | `5 not in [1, 2, 3, 4, 6]` </br>`# True` | `!mixedData.includes('not_exist')` </br>`// true` |
|  | `` | `` |

## 2.3. __Tuple__

| Function | Python | JavaScript |
| --- | ------ | ---- |
| Tuple | `location = (13.4125, 103.866667)` | `` |
|  | `length, width, height = 52, 40, 100` | `` |
|  | `dimensions = 52, 40, 100` | `` |
| Tuple Unpacking | `length, width, height = dimensions` | `` |
|  | `` | `` |
|  | `` | `` |


## 2.4. __Sets__

| Function | Python | JavaScript |
| --- | ------ | ---- |
| Sets | `fruit = set()` | `const fruit = new Set();` |
|  | `fruit = {"apple", "banana", "orange", "grapefruit"}` | `const fruit = new Set(["apple", "banana", "orange", "grapefruit"])` |
| Remove duplicates | `numbers = [1, 2, 6, 3, 1, 1, 6]`    | `const numbers = [1, 2, 6, 3, 1, 1, 6]`   |
|  | `unique_nums = set(numbers)` | `unique_nums = new Set(numbers)` |
|  | `# {1, 2, 3, 6}` | `// {1, 2, 6, 3}` |
| check for element | `"watermelon" in fruit` | `fruit.has("watermelon")` |
| add an element | `fruit.add("watermelon")` | `fruit.add("watermelon")` |
| remove an element | `fruit.remove("apple")` </br>`//if present`  | `fruit.delete('apple') //true` |
|  | `fruit.discard("apple")` </br>`//if not sure`  |  |
| remove a random element | `fruit.pop()` </br>`# 'apple'(random)` |  |
| Union | `` | `` |
| intersection | `` | `` |
| difference | `` | `` |
| clear Set | `fruit.clear()` | `fruit.clear()` |
| length of set | `len(fruit)` | `fruit.size` |

## 2.5. __Dictionaries/Object__

| Function | Python | JavaScript |
| --- | ------ | ---- |
| create dictionary | `elements = dict()` | `const elements = new Object();` |
|  | `elements = {}` | `const elements = {};` |
|  | `elements = {"hydrogen": 1, "helium": 2, "carbon": 6}` | `const elements = {"hydrogen": 1, "helium": 2, "carbon": 6};` |
| Check Keys in dict | `"carbon" in elements` | `"carbon" in elements` |
| | | `elements.hasOwnProperty('carbon')` |
| pull values from keys | `elements["helium"]` </br>`# 2`  `elements["kryptonite"]` </br>`# KeyError`| `elements["helium"]` </br>`# 2`  `elements["kryptonite"]` </br>`# undefined` |
|  | | `elements.helium` </br>`# 2` |
| pull values from key or return (None/user defined msg)  | `elements.get('kryptonite', 'There\'s no such element!')` | `` |
| add values to the dictionary | `` | `` |
| length of dict | `len(elements)` | `Object.keys().length` |
| sort values by keys | `sorted(elements)` | `Object.keys().sort()` |
| First Value of sorted key | `max(elements)` | `Object.keys().sort()[0]` |
| Last Value of sorted key | `min(elements)` | `Object.keys().sort()[Object.keys().length -1]` |
| list of values | `.values()` | `Object.keys().map( word => [word])` |

## 2.6. __Compound Data Structures__


 **i. create Coumpound**
```python
# PYTHON
elements = {"hydrogen": {"number": 1,
                         "weight": 1.00794,
                         "symbol": "H"},
              "helium": {"number": 2,
                         "weight": 4.002602,
                         "symbol": "He"}}
```
```javascript
// ES6
const elements = {"hydrogen": {"number": 1,
                         "weight": 1.00794,
                         "symbol": "H"},
              "helium": {"number": 2,
                         "weight": 4.002602,
                         "symbol": "He"}}
```
```javascript
// ES6 Array of Objects
const elementsArray = [ {"number": 1,
                         "weight": 1.00794,
                         "symbol": "H"},
                         {"number": 2,
                         "weight": 4.002602,
                         "symbol": "He"}]
```
**ii. access Element** 
```python
# PYTHON
hydrogen_weight = elements["hydrogen"]["weight"]  # get hydrogen's weight
```
```javascript
// ES6
hydrogen_weight = elements["hydrogen"]["weight"]
hydrogen_weight = elements.hydrogen.weight  
// get hydrogen's weight
```
**iii. add a new key to the dictionary** 
```python
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
 
```
```javascript
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
 
```

## 3. __Control Flow/ Conditional Operator__

__i. *if*__
```python
# python
if expression:
    pass
```
```javascript
// Es6
if (condition) {
    
}
```

__ii. *if else*__
```python
# python
if condition:
    pass
else:
    pass
```
```javascript
// Es6
if (condition) {
    
} else {
    
}
```

__iii. *else if*__
```python
# python
if condition:
    pass
elif expression:
    pass
elif expression:
    pass
else:
    pass
```
```javascript
// Es6
if (condition) {
    
} else if (condition) {
    
} else if (condition) {
    
} else {
    
}
```

__iv. *Ternary Operator*__
```python
# python
a, b = 10, 20
  
# Copy value of a in min if a < b else copy b 
min = a if a < b else b 
  
print(min) 
```
```javascript
// Es6
const [a,b] = [10,20]
const min = (a<b)?a:b
console.log(min)
```
__iv. *Switch*__
```python
# python
def week(i):
        switcher={
                0:'Sunday',
                1:'Monday',
                2:'Tuesday',
                3:'Wednesday',
                4:'Thursday',
                5:'Friday',
                6:'Saturday'
             }
         return switcher.get(i,"Invalid day of week")
```
```javascript
// Es6
function week(i) {
    switch (i) {
        case 0:
            return "sunday"
            break;
        case 1:
            return "Monday"
            break;
        case 2:
            return "Tuesday"
            break;
        case 3:
            return "Wednesday"
            break;
        case 4:
            return "Thursday"
            break;
        case 5:
            return "Friday"
            break;
        case 6:
            return "Saturday"
            break;    
        default:
            return "Invalid day of week"
    }
}
```
