# Syntax, Data Structures, and JSON in Go, Java, JavaScript, and Python - KEPLOY DEVREL COHORT 3.0

This cheat sheet provides basic syntax examples, loops, functions, and data structures in Go, Java, JavaScript, and Python.

## Basic Syntax (Printing Hello World!)

### Go
```go
package main

import "fmt"

func main() {
    var message string = "Hello, World!"
    fmt.Println(message)
}
```
### Java

```
public class Main {
    public static void main(String[] args) {
        String message = "Hello, World!";
        System.out.println(message);
    }
}
```

### JavaScript

```
let message = "Hello, World!";
console.log(message);
```

### Python

```
message = "Hello, World!"
print(message)
```

## Variable Declaration

### Go

```
package main

import "fmt"

func main() {
    // Declare and initialize a string variable
    message := "Hello, World!"
    fmt.Println(message)

    // Declare a string variable without initializing it
    var greeting string
    greeting = "Welcome"
    fmt.Println(greeting)

    // Declare and initialize a numeric variable
    age := 30
    fmt.Println(age)

    // Declare multiple variables at once
    var (
        name     string = "Alice"
        location string = "Wonderland"
    )
    fmt.Println(name, location)
}
```

### Java
```
public class Main {
    public static void main(String[] args) {
        // Declare and initialize a string variable
        String message = "Hello, World!";
        System.out.println(message);

        // Declare a string variable without initializing it
        String greeting;
        greeting = "Welcome";
        System.out.println(greeting);

        // Declare and initialize a numeric variable
        int age = 30;
        System.out.println(age);

        // Declare multiple variables at once
        String name = "Alice", location = "Wonderland";
        System.out.println(name + " " + location);
    }
}
```

### JavaScript

```
// Declare and initialize a string variable
let message = "Hello, World!";
console.log(message);

// Declare a string variable without initializing it
let greeting;
greeting = "Welcome";
console.log(greeting);

// Declare and initialize a numeric variable
let age = 30;
console.log(age);

// Declare multiple variables at once
let name = "Alice", location = "Wonderland";
console.log(name + " " + location);
```
### Python

```
# Declare and initialize a string variable
message = "Hello, World!"
print(message)

# Declare a string variable without initializing it
greeting = str()
greeting = "Welcome"
print(greeting)

# Declare and initialize a numeric variable
age = 30
print(age)

# Declare multiple variables at once
name, location = "Alice", "Wonderland"
print(name, location)
```

## Loops

### Go

```
package main

import "fmt"

func main() {
    // For loop
    for i := 0; i < 5; i++ {
        fmt.Println(i)
    }

    // While loop (using for loop)
    j := 0
    for j < 5 {
        fmt.Println(j)
        j++
    }

    // Infinite loop (using for loop)
    k := 0
    for {
        fmt.Println(k)
        k++
        if k == 5 {
            break
        }
    }

    // For-each loop
    numbers := []int{1, 2, 3, 4, 5}
    for index, number := range numbers {
        fmt.Println(index, number)
    }
}
```

### Java

```
public class Main {
    public static void main(String[] args) {
        // For loop
        for (int i = 0; i < 5; i++) {
            System.out.println(i);
        }

        // While loop
        int j = 0;
        while (j < 5) {
            System.out.println(j);
            j++;
        }

        // Do-while loop
        int k = 0;
        do {
            System.out.println(k);
            k++;
        } while (k < 5);

        // For-each loop
        int[] numbers = {1, 2, 3, 4, 5};
        for (int index = 0; index < numbers.length; index++) {
            int number = numbers[index];
            System.out.println(index + " " + number);
        }
    }
}

```
### JavaScript

```
// For loop
for (let i = 0; i < 5; i++) {
    console.log(i);
}

// While loop
let j = 0;
while (j < 5) {
    console.log(j);
    j++;
}

// Do-while loop
let k = 0;
do {
    console.log(k);
    k++;
} while (k < 5);

// For-each loop (using for-of loop)
let numbers = [1, 2, 3, 4, 5];
for (let [index, number] of numbers.entries()) {
    console.log(index, number);
}

```

### Python

```
# For loop
for i in range(5):
    print(i)

# While loop
j = 0
while j < 5:
    print(j)
    j += 1

# For-each loop (using for loop)
numbers = [1, 2, 3, 4, 5]
for index in range(len(numbers)):
    number = numbers[index]
    print(index, number)

# For-each loop (using for-in loop)
for index, number in enumerate(numbers):
    print(index, number)
```

## Functions
### Go
```
// Define a function that takes two integers and returns their sum
func add(a, b int) int {
    return a + b
}

// Call the function
sum := add(3, 4) // sum = 7
```

### Java
```
// Define a function that takes two integers and returns their sum
public int add(int a, int b) {
    return a + b;
}

// Call the function
int sum = add(3, 4); // sum = 7
```

### JavaScript
```
// Define a function that takes two integers and returns their sum
function add(a, b) {
    return a + b;
}

// Call the function
var sum = add(3, 4); // sum = 7
```

### Python
```
# Define a function that takes two integers and returns their sum
def add(a, b):
    return a + b

# Call the function
sum = add(3, 4) # sum = 7
```

## Data Sructures
### Go
### Arrays

<i>An array is a collection of elements of the same type that are stored in contiguous memory locations.</i> 

```
package main

import "fmt"

func main() {
    // Declaring an array of integers
    var numbers [5]int

    // Initializing an array
    numbers = [5]int{1, 2, 3, 4, 5}

    // Accessing elements of an array
    fmt.Println(numbers[0]) // Output: 1
    fmt.Println(numbers[4]) // Output: 5

    // Modifying elements of an array
    numbers[0] = 10
    fmt.Println(numbers) // Output: [10 2 3 4 5]
}

```

### Slices
<i>A slice is a dynamic array whose size can grow or shrink during runtime.</i>

```
package main

import "fmt"

func main() {
    // Declaring a slice of integers
    var numbers []int

    // Initializing a slice
    numbers = []int{1, 2, 3, 4, 5}

    // Accessing elements of a slice
    fmt.Println(numbers[0]) // Output: 1
    fmt.Println(numbers[4]) // Output: 5

    // Modifying elements of a slice
    numbers[0] = 10
    fmt.Println(numbers) // Output: [10 2 3 4 5]

    // Appending elements to a slice
    numbers = append(numbers, 6, 7, 8)
    fmt.Println(numbers) // Output: [10 2 3 4 5 6 7 8]

    // Slicing a slice
    slice := numbers[2:5]
    fmt.Println(slice) // Output: [3 4 5]

    // Length and capacity of a slice
    fmt.Println(len(numbers)) // Output: 8
    fmt.Println(cap(numbers)) // Output: 8
}
```
### Maps
<i>A map is an unordered collection of key-value pairs where all keys are of the same type and all values are of the same type, but the keys and values can be of different types from each other.</i>

```
package main

import "fmt"

func main() {
    // Declaring a map of strings to integers
    var scores map[string]int

    // Initializing a map
    scores = map[string]int{
        "Alice": 95,
        "Bob":   80,
        "Charlie": 70,
    }

    // Accessing elements of a map
    fmt.Println(scores["Alice"]) // Output: 95

    // Modifying elements of a map
    scores["Bob"] = 85
    fmt.Println(scores) // Output: map[Alice:95 Bob:85 Charlie:70]

    // Adding elements to a map
    scores["David"] = 90
    fmt.Println(scores) // Output: map[Alice:95 Bob:85 Charlie:70 David:90]

    // Deleting elements from a map
    delete(scores, "Charlie")
    fmt.Println(scores) // Output: map[Alice:95 Bob:85 David:90]
}

```

### Structs
<i>A struct is a composite data type that groups together zero or more values with different types.</i>
```
package main

import "fmt"

// Defining a struct type
type Person struct {
    Name    string
    Age     int
    Address string
}

func main() {
    // Initializing a struct
    person := Person{
        Name:    "Alice",
        Age:     25,
        Address: "123 Main St",
    }

    // Accessing fields of a struct
    fmt.Println(person.Name)    // Output: Alice
    fmt.Println(person.Age)     // Output: 25
    fmt.Println(person.Address) // Output: 123 Main St

    // Modifying fields of a struct
    person.Age = 26
    fmt.Println(person) // Output: {Alice 26 123 Main St}
}
    
```

### Pointers

<i>A pointer is a variable that stores the memory address of another variable.</i>

```
package main

import "fmt"

func main() {
    // Declaring a pointer variable
    var ptr *int

    // Declaring a regular variable
    var number int = 42

    // Assigning the address of the regular variable to the pointer variable
    ptr = &number

    // Accessing the value of the regular variable through the pointer variable
    fmt.Println(*ptr) // Output: 42

    // Modifying the value of the regular variable through the pointer variable
    *ptr = 43
    fmt.Println(number) // Output: 43
}

```


### Java

### Arrays
<i>An array is a collection of elements of the same type, stored in contiguous memory locations. Arrays are used to store and manipulate collections of data that are of the same type.</i>
```
// Initializing an array of integers
int[] arr = {1, 2, 3, 4, 5};

// Accessing an element of the array
System.out.println(arr[2]); // Output: 3

// Modifying an element of the array
arr[2] = 6;
System.out.println(arr[2]); // Output: 6

```
### ArrayList
<i>An ArrayList is a dynamic array implementation that allows for the addition and removal of elements at runtime. ArrayLists can store elements of any type, including objects.</i>
```
// Initializing an ArrayList of integers
ArrayList<Integer> list = new ArrayList<>();

// Adding elements to the ArrayList
list.add(1);
list.add(2);
list.add(3);

// Accessing an element of the ArrayList
System.out.println(list.get(1)); // Output: 2

// Modifying an element of the ArrayList
list.set(1, 4);
System.out.println(list.get(1)); // Output: 4
```

### LinkedList
<i>A LinkedList is a data structure that stores elements in nodes, each of which contains a reference to the next node in the list. LinkedLists can be used to implement queues and stacks, among other things.</i>
```
// Initializing a LinkedList of strings
LinkedList<String> list = new LinkedList<>();

// Adding elements to the LinkedList
list.add("Alice");
list.add("Bob");
list.add("Charlie");

// Accessing an element of the LinkedList
System.out.println(list.get(1)); // Output: Bob

// Modifying an element of the LinkedList
list.set(1, "Dave");
System.out.println(list.get(1)); // Output: Dave
```
### HashMap
<i>A HashMap is a data structure that stores key-value pairs. HashMaps provide constant-time performance for the basic operations (add, remove, and get) on average, making them a popular choice for many applications.</i>
```
// Initializing a HashMap of strings and integers
HashMap<String, Integer> map = new HashMap<>();

// Adding key-value pairs to the HashMap
map.put("Alice", 25);
map.put("Bob", 30);
map.put("Charlie", 35);

// Accessing a value from the HashMap
System.out.println(map.get("Bob")); // Output: 30

// Modifying a value in the HashMap
map.put("Bob", 40);
System.out.println(map.get("Bob")); // Output: 40
```

### JavaScript

### Arrays
<i>An array is a collection of elements of the same type, stored in contiguous memory locations. Arrays are used to store and manipulate collections of data that are of the same type.</i>

```
// Initializing an array of integers
let arr = [1, 2, 3, 4, 5];

// Accessing an element of the array
console.log(arr[2]); // Output: 3

// Modifying an element of the array
arr[2] = 6;
console.log(arr[2]); // Output: 6
```

### Objects
<i>An object is a collection of key-value pairs, where each key is a string and each value can be of any type, including other objects.</i>
```
// Initializing an object
let obj = {
  name: "Alice",
  age: 25,
  city: "New York"
};

// Accessing a value from the object
console.log(obj.age); // Output: 25

// Modifying a value in the object
obj.age = 30;
console.log(obj.age); // Output: 30
```
### Maps
<i>A Map is a collection of key-value pairs, where each key can be of any type, including objects, and each value can be of any type.</i>
```
// Initializing a Map of strings and integers
let map = new Map();

// Adding key-value pairs to the Map
map.set("Alice", 25);
map.set("Bob", 30);
map.set("Charlie", 35);

// Accessing a value from the Map
console.log(map.get("Bob")); // Output: 30

// Modifying a value in the Map
map.set("Bob", 40);
console.log(map.get("Bob")); // Output: 40
```

### Sets
<i>A Set is a collection of unique values of any type.</i>
```
// Initializing a Set of integers
let set = new Set();

// Adding elements to the Set
set.add(1);
set.add(2);
set.add(3);

// Checking if an element exists in the Set
console.log(set.has(2)); // Output: true

// Removing an element from the Set
set.delete(2);
console.log(set.has(2)); // Output: false
```
### Python
### Lists
<i>A list is a collection of elements of the same or different types, stored in ordered sequence. Lists are used to store and manipulate collections of data that are of variable length</i>
```
# Initializing a list of integers
my_list = [1, 2, 3, 4, 5]

# Accessing an element of the list
print(my_list[2]) # Output: 3

# Modifying an element of the list
my_list[2] = 6
print(my_list[2]) # Output: 6
```
### Tuples
<i>A tuple is a collection of elements of the same or different types, stored in ordered sequence. Tuples are immutable, which means that their contents cannot be modified after they are created.</i>
```
# Initializing a tuple of integers
my_tuple = (1, 2, 3, 4, 5)

# Accessing an element of the tuple
print(my_tuple[2]) # Output: 3
```
### Dictionaries
<i>A dictionary is a collection of key-value pairs, where each key is a unique string and each value can be of any type.</i>
```
# Initializing a dictionary
my_dict = {
  "name": "Alice",
  "age": 25,
  "city": "New York"
}

# Accessing a value from the dictionary
print(my_dict["age"]) # Output: 25

# Modifying a value in the dictionary
my_dict["age"] = 30
print(my_dict["age"]) # Output: 30

```

### Sets
<i>A set is a collection of unique elements of any type.</i>
```
# Initializing a set of integers
my_set = {1, 2, 3, 4, 5}

# Adding an element to the set
my_set.add(6)

# Checking if an element exists in the set
print(2 in my_set) # Output: True

# Removing an element from the set
my_set.remove(2)
print(2 in my_set) # Output: False
```

## JSON encoding/decoding

### Go
#### Encoding JSON
To encode a Go data structure into JSON, you can use the json.Marshal function. This function takes a Go value as input and returns a byte slice containing the JSON-encoded data.

```
import "encoding/json"

type Person struct {
    Name    string `json:"name"`
    Age     int    `json:"age"`
    Address string `json:"address"`
}

// Create a Person object
p := Person{Name: "Alice", Age: 30, Address: "123 Main St"}

// Encode the Person object into JSON
data, err := json.Marshal(p)
if err != nil {
    panic(err)
}

// Print the JSON-encoded data
fmt.Println(string(data))

```

#### Decoding JSON
To decode a JSON string into a Go data structure, you can use the json.Unmarshal function. This function takes a byte slice containing the JSON data as input and a pointer to a Go value that will be populated with the decoded data.

```
// Decode the JSON-encoded data into a Person object
var decoded Person
err = json.Unmarshal(data, &decoded)
if err != nil {
    panic(err)
}

// Print the decoded Person object
fmt.Println(decoded.Name)
fmt.Println(decoded.Age)
fmt.Println(decoded.Address)
```
<i>In addition to encoding and decoding structs, the encoding/json package also provides functions for encoding and decoding other Go data types, such as maps and slices.</i>

### Java
In Java, you can use the Jackson library for encoding and decoding JSON data. Here are some examples of encoding and decoding JSON using Jackson:

#### Encoding JSON
To encode a Java object into JSON, you can use the ObjectMapper class from Jackson. This class provides methods for converting Java objects to JSON and vice versa.

```
import com.fasterxml.jackson.databind.ObjectMapper;

public class Person {
    private String name;
    private int age;
    private String address;

    // getters and setters
}

// Create a Person object
Person person = new Person();
person.setName("Alice");
person.setAge(30);
person.setAddress("123 Main St");

// Encode the Person object into JSON
ObjectMapper objectMapper = new ObjectMapper();
String json = objectMapper.writeValueAsString(person);

// Print the JSON-encoded data
System.out.println(json);
```
#### Decoding JSON
To decode a JSON string into a Java object, you can use the ObjectMapper class from Jackson.

```
// Decode the JSON-encoded data into a Person object
String json = "{\"name\":\"Alice\",\"age\":30,\"address\":\"123 Main St\"}";
Person decoded = objectMapper.readValue(json, Person.class);

// Print the decoded Person object
System.out.println(decoded.getName());
System.out.println(decoded.getAge());
System.out.println(decoded.getAddress());
```

### JavaScript

#### Encoding JSON
To encode a JavaScript object into JSON, you can use the JSON.stringify() method. This method takes a JavaScript value as input and returns a string containing the JSON-encoded data.

```
const person = { name: "Alice", age: 30, address: "123 Main St" };

// Encode the Person object into JSON
const json = JSON.stringify(person);

// Print the JSON-encoded data
console.log(json);
```

#### Decoding JSON
To decode a JSON string into a JavaScript object, you can use the JSON.parse() method. This method takes a string containing the JSON data as input and returns a JavaScript object containing the decoded data.

```
// Decode the JSON-encoded data into a Person object
const json = '{"name":"Alice","age":30,"address":"123 Main St"}';
const decoded = JSON.parse(json);

// Print the decoded Person object
console.log(decoded.name);
console.log(decoded.age);
console.log(decoded.address);
```

### Python
#### Encoding JSON
To encode a Python object into JSON, you can use the json.dumps() method. This method takes a Python object as input and returns a string containing the JSON-encoded data.
```

import json

person = {"name": "Alice", "age": 30, "address": "123 Main St"}

# Encode the Person object into JSON
json_data = json.dumps(person)

# Print the JSON-encoded data
print(json_data)
```

#### Decoding JSON
To decode a JSON string into a Python object, you can use the json.loads() method. This method takes a string containing the JSON data as input and returns a Python object containing the decoded data.

```
# Decode the JSON-encoded data into a Person object
json_data = '{"name": "Alice", "age": 30, "address": "123 Main St"}'
decoded = json.loads(json_data)

# Print the decoded Person object
print(decoded["name"])
print(decoded["age"])
print(decoded["address"])
```