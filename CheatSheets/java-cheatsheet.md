# Table of Content

- [Data Types](#data-types)
- [Data Conversion](#data-conversion)
- [Operators](#operators)
- [Statements](#statements)
- [Arrays](#arrays)
- [Strings](#strings)
- [String Methods](#string-methods)
- [StringTokenizer](#stringtokenizer)
- [Collection](#Collection)

## Data Types

| Data Type | Size   |
| --------- | ------ |
| boolean   | 1 bit  |
| char      | 2 byte |
| int       | 4 byte |
| short     | 2 byte |
| long      | 8 byte |
| float     | 4 byte |
| double    | 8 byte |

**[🔼Back to Top](#table-of-contents)**

## Data Conversion

### String to Number

```java
        int i = Intege­r.p­ars­eInt(_str_);
 	double d = Double.pa­rse­Double(_str_);
```

### Any Type to String

```java
 	String s = String.va­lueOf(_value_);

```

### Numeric Conver­sions

```java
 	int i = (int) _numeric expression_;
        double i = (double) _numeric expression_;
        long i = (long) _numeric expression_;
```

**[🔼Back to Top](#table-of-contents)**

## Operators

| Operator Category                | Operators                                          |
| -------------------------------- | -------------------------------------------------- |
| Arithmetic operators             | +, -, /, \*, %                                     |
| Relational operators             | <, >, <=, >=,==, !=                                |
| Logical operators                | &&, \|\|                                           |
| Assignment operator              | =, +=, −=, ×=, ÷=, %=, &=, ^=, \|=, <<=, >>=, >>>= |
| Increment and Decrement operator | ++ , - -                                           |
| Conditional operators            | ?, :                                               |
| Bitwise operators                | ^, &, \|                                           |
| Special operators                | . (dot operator to access methods of class)        |

**[🔼Back to Top](#table-of-contents)**

## Statements

### If Statement

```java
if ( _expression_ ) {
­ _statements_
} else if ( _expression_ ) {
­ _statements_
} else {
­ _statements_
}
```

### While Loop

```java
while ( _expression_ ) {
­ _statements_
}
```

### Do-While Loop

```java
do {
­ _statements_
} while ( _expression_ );
```

### For Loop

```java
for ( int i = 0; i < _max_; ++i) {
­ _statements_
}
```

### For Each Loop

```java
for ( _var_ : _collection_ ) {
­ _statements_
}
```

### Switch Statement

```java
switch ( _expression_ ) {
­ case _value_:
­ ­ ­ _statements_
­ ­ ­ ­break;
­ case _value2_:
­ ­ ­ _statements_
­ ­ ­ ­break;
­ ­def­ault:
­ ­ ­ _statements_
}
```

### Exception Handling

```java
try {
­ ­sta­tem­ents;
} catch (_Except­ionType_  _e1_) {
­ ­sta­tem­ents;
} catch (Exception _e2_) {
­ ­cat­ch-all statem­ents;
} finally {
­ ­sta­tem­ents;
}
```

**[🔼Back to Top](#table-of-contents)**
## Arrays

### Initialisation
#### For 1-D array
```java
// datatype array_name[] = new datatype[Size];
int number[] = new int[10];           // An Integer Array
String characters[] = new String[10]; // A String array
int[] number = new int[]{ 1,2,3,4,5,6,7,8,9,10 }; 
```
#### For 2-D array
```java
// datatype array_name[][] = new datatype[row][column];
int number[][] = new int[10][10];            // An Integer Array of dimensions 10 x 10
String characters[][] = new String[10][10];  // An String Array of dimensions 10 x 10
```

### Traversal
```java
// Traditional for loop
for(int i=0;i<number.length;i++) //length gives the size of the array
{ 
System.out.println(number[i]);
}
// Advanced for loop
for(int i:number)  
{
System.out.println(i);  
}
```

**[🔼Back to Top](#table-of-contents)**


## Strings
#### "In Java, string is basically an object that represents sequence of char values. An array of characters works same as Java string." : Javatpoint

### Ways to Initialise a string

### Using String Literal
```java
String s = "INPUT";
//Using the new keyword
String s = new String("INPUT");
//From a given character array
char ch[]={'I','N','P','U','T'};    
String s=new String(ch);   
```
The above mentioned methods creates a string that are immutable, to make strings mutable, we can use StringBuilder or StringBuffer

### Using StringBuffer
##### "The string represents fixed-length, immutable character sequences while StringBuffer represents growable and writable character sequences." : GFG
```java
//Create a StringBuffer Object, i.e., empty string buffer
//By default it can take up a sequence of 16 characters
StringBuffer sb = new StringBuffer();  
// Can be initialised with a string
StringBuffer sb2 = new StringBuffer("Input");
```
##### 1) append(string_data) method : Used to concatenate the entered string and the strings in the buffer
```java
sb.append("Input");  //Now the empty string has been modified to "Input"
```
##### 2) insert(beginIndex, endIndex, string_data) method : Inserts a given string literal to the specified positions
```java
sb.insert(2," A String");
//Now String is "In A Stringput"
```

##### 3) replace(beginIndex, endIndex, string_data) method : Use to replace a sequence of characters from the specified beginIndex and endIndex-1, with another sequence
```java
sb.replace(11,14," Literal");  
//Now String is "In A String Literal"
```

##### 4) delete(beginIndex, endIndex) method : Use to delete a sequence of characters from the specified beginIndex and endIndex-1
```java
sb.delete(11,19);
//Now the string is "In A String"
```
##### 5) reverse() method : Reverses the current string
```java
sb.reverse();
// Now the String is "gnirtS A nI"
```

### Using StringBuilder
##### Very similiar to the StringBuffer class but is not Synchronous and neither Thread-Safe. But high in performance, i.e., speedy
```java
//Create a StringBuilder Object, i.e., StringBuilder with no characters
//By default it can take up a sequence of 16 characters
StringBuilder sb = new StringBuilder(); 
StringBuilder sb2 = new StringBuffer("Input");
```
##### append(),  insert(), replace(), delete(), reverse() are used in the same way as used in the StringBuffer
##### To convert the objects of either StringBuilder or StringBuffer to string, use : toString()
```java
String str = sb.toString();
System.out.println(str);
```
**[🔼Back to Top](#table-of-contents)**

## String Methods

| Command                    | Description                        |
| -------------------------- | ---------------------------------- |
| length                     | length of string                   |
| charAt(_i_)                | extract \_i_th character           |
| subst­ring(_start_, _end_) | substring from _start_ to _end_-1  |
| toUpp­erC­ase()            | returns copy of _s_ in ALL CAPS    |
| toLow­erC­ase()            | returns copy of _s_ in lowercase   |
| indexOf(_x_)               | index of first occurence of _x_    |
| replace(_old_, _new_)      | search and replace                 |
| split(_regex_)             | splits string into tokens          |
| trim()                     | trims surrou­nding whitespace      |
| equals(_s2_)               | true if s equals s2                |
| compa­reTo(_s2_)           | 0 if equal/+ if s > s2/- if s < s2 |


## StringTokenizer
#### A class in java that is used to break a string into tokens based on given delimeter(s), by default breaks at whitespaces

### Initialising
```java
// To break the string at whitespaces, use the following code
StringTokenizer st = new StringTokenizer(string_value_or_variable);
// To break the string at multiple delimeters, use the following code
StringTokenizer st = new StringTokenizer(string_value_or_variable, delimiter_string);
```
### Functions available in the StringTokeniser Class

| Command                    | Description                                         |
| -------------------------- | --------------------------------------------------- |
| countTokens()              | Returns the number of tokens present                |
| hasMoreToken()             | Checks if there are more tokens in the string       |
| nextElement()              | Return the object of the next element in the stream |
| hasMoreElements()          | Checks if there are more elements in the string     |
| nextToken()                | Returns the next token from the StringTokenizer.    |


#### Example to break the string at whitespaces
```java
StringTokenizer st = new StringTokenizer("Hy there, how are you? Hoping you are doing great!");
while (st.hasMoreTokens())
{
	System.out.print(st.nextToken() + " ; ");
}
```
#### Output : Hy ; there, ; how ; are ; you? ; Hoping ; you ; are ; doing ; great! ;
The semi colon is used to seperate the tokens

#### Example to break the string at multiple delimeters
```java
// The following scheme can be used to break a punctuated string, into words
StringTokenizer st = new StringTokenizer("Hy there, how are you? Hoping you are doing great!", ":,!? ");
while (st.hasMoreTokens())
{
	System.out.print(st.nextToken() + " ; ");
}
```
#### Output : Hy ; there ; how ; are ; you ; Hoping ; you ; are ; doing ; great ;
The semi colon is used to seperate the tokens

**[🔼Back to Top](#table-of-contents)**

## Collection

### List

| Type       | Declaration                        |
| ---------- | ---------------------------------- |
| ArrayList  | List<E> arr = new ArrayList<E>();  |
| LinkedList | List<E> arr = new LinkedList<E>(); |
     

### Set

| Type          | Declaration                       |
| ------------- | --------------------------------- |
| HashSet       | Set<E> set = new HashSet<E>();    |
| TreeSet       | Set<E> set = new TreeSet<E>();    |
| LinkedHashSet | Set<E> set = new LinkedHashSet(); |
     
### Operations on List and Set
     
| Method     | Description                               | Declaration               |
| ---------- | ----------------------------------------- | ------------------------- |
| add        | To add an element into the list           | arr.add(element)          |
| remove     | To remove an element into the list        | arr.remove(element)       |
| get        | To get an element at particular index     | arr.get(element)          |
| set        | To set the element at a particular index  | arr.set(index, element)   |
| size       | To get size of the list                   | arr.size()                |
| contains   | To check if the list contains the element | arr.contains(element)     |
| indexOf    | To get the index of the element           | arr.indexOf(element)      |

### Map

| Type          | Declaration                                              |
| ------------- | -------------------------------------------------------- |
| LinkedHashMap | LinkedHashMap<E> linkedHashMap = new LinkedHashMap<E>(); |
| HashMap       | HashMap<E> hashMap = new HashMap<E>();                   |
| TreeMap       | TreeMap<K> treeMap = new TreeMap<E>();                   |

### Queue

| Type          | Declaration                                           |
| ------------- | ----------------------------------------------------- |
| Queue         | Queue<E> queue = new LinkedList();                    |
| PriorityQueue | PriorityQueue<E> priorityQueue = new PriorityQueue(); |
| ArrayDeque    | ArrayDeque<E> arrayDeque = new ArrayDeque();          |

**[🔼Back to Top](#table-of-contents)**
