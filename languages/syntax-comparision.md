- [Data Types](#data-types)
  - [Primitive Data Types](#primitive-data-types)
  - [Array / Collection](#array--collection)
    - [Array](#array)
- [Comments](#comments)
  - [Single-line comment](#single-line-comment)
  - [Multi-line comment](#multi-line-comment)
  - [Documentation comment](#documentation-comment)
- [Control Statements](#control-statements)
  - [Conditional Statements](#conditional-statements)
    - [If Else Condition](#if-else-condition)
    - [Switch Condition](#switch-condition)
  - [Loop](#loop)
    - [For Loop](#for-loop)
    - [For In Loop](#for-in-loop)
    - [For Of Loop](#for-of-loop)
    - [For Each Loop](#for-each-loop)
    - [While Loop](#while-loop)
    - [Do While Loop](#do-while-loop)
    - [Break Statement](#break-statement)
    - [Continue Statement](#continue-statement)
- [References:](#references)

# Data Types

## Primitive Data Types

| Data Type | Java                                      | JavaScript   | C#
| ---       | ---                                       | ---          | ---
| Boolean   | `boolean var_name = false;`               |
| Character | `char var_name = 'A'; // 16bit Unicode`   | 
| Byte      | `byte var_name = -2^7`                    | 
| Short     | `short var_name = -2^15;`                 | 
| Integer   | `int var_name = -2^31;`                   | 
| Long      | `long var_name = -2^63L`                  | 
| Float     | `float var_name = -32f;`                  | 
| Double    | `double var_name = -64d`                  | 

## Array / Collection

### Array

```java
    // Java

    int[] var_name = new int[size];
    int[][] var_name = new int[row_size][col_size];

    int arr[] = { 33, 3, 4, 5 };

    int[] copiedArray = new int[3];
    System.arraycopy(arr, 0, copiedArray, 0, 3); // Copy Array
    int clonedArray[] = arr.clone();             // Clone Array
```

```js


```

# Comments

## Single-line comment

`// comment line`

## Multi-line comment

```js
    /*
        comment line 1
        comment line 2
    */
```

## Documentation comment

```js
    /**
        Description: Describe intent
        @param param1   purpose1
        @param param2   purpose 2
    */
```

# Control Statements

## Conditional Statements

### If Else Condition

> JavaScript
```js
    if (expression) {
        // statements
    } else if (expression) {
        // statements
    } else {
        // statements
    }
```

### Switch Condition

```js
    switch (expression) {
        case value1:
            // code block
            break;  // If break is removed below case will also be executed
        case value2:    
            // code block
            break;
        default:
            // code block
    }
```

## Loop

### For Loop

```js
    for (initialization_statement; condition_statement; post_execution_statement) {
        // code block
    }
```
> Supported by Java, C#

### For In Loop

```js
    for (index in array) {
       // code block can access array by index
    }
```

### For Of Loop

```js
    for (item of items_array) {
    // code block
    }
```

### For Each Loop

```java
    // Java

    for (int item:intArray) {
        System.out.println(i);
    }
```

> JavaScript supports `Array.forEach(item => { })`

### While Loop

```js
    while (condition) {
       // code block
    }
```

> Supported by Java, C#

### Do While Loop

```js
    //Executed at least once even if condition is false
    do {
        // code block
    }
    while (condition);
```

> Supported by Java, C#
> 
### Break Statement

`break;`

> Supported by Java, C#

### Continue Statement

`continue`

> Supported by Java, C#

# References:

