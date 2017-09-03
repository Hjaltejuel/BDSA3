# Assignment #3: Week 37

## Introduction to Software Engineering

### Exercise 1

Question...

## C&#35;

Fork this repository and implement the code required for the assignments below.

### Extension Methods

Consider the two methods you implemented last week:

```csharp
IEnumerable<T> Flatten<T>(IEnumerable<IEnumerable<T>> items)

IEnumerable<T> Filter<T>(IEnumerable<T> items, Predicate<T> predicate)
```

Given the following collections in scope:

```
IEnumerable<int>[] xs;

int[] ys;
```

Solve the following questions with extension methods (one-liners):

1. Flatten the numbers in `xs`.
2. Select numbers in `ys` which are divisible by `7` and greater than `42`.
3. Select numbers in `ys` which are *leap years*.  

Write the answers in the ANSWERS.md file.

Implement and test the following extension methods:

1. A method `IsSecure` which extends `Uri` and returns true if the `Uri` is using *Secure Hypertext Transfer Protocol*.

2. A method `WordCount` which extends `string` and returns the number of words in the string. Note a word can only contain *unicode letters* (no numbers or symbols).

Use the supplied `Extensions.cs` and `ExtensionsTests.cs` files.

### Delegates / Anonymous methods

Implement the following anonymous functions using the built-in delegates and lambda expressions: 

1. A method which takes a string and prints the content in reverse order (by character)
2. A method which takes two decimals and returns the product
3. A method which takes a whole number and a string and returns `true` if they are numerically equal. Note that the string `"  0042"` should return true if the number is `42`

Write the answers in the ANSWERS.md file.

You probably want to implement a set of tests to validate the methods.

Use the supplied `DelegatesTests.cs` file. 

### LINQ

Given the following class:

```csharp
public class Wizard
{
    public string Name { get; set; }

    // Book or film or...
    public string Medium { get; set; }

    public int? Year { get; set; }

    public string Author { get; set; }
}
```

Use the supplied `Queries.cs` and corresponding tests class to implement and test the following queries using LINQ:
(You need to wrap the queries in suitable methods for testing)

1. Wizards invented by *Rowling* after *2002*. Only return the names.
2. The year the first *sith lord* was introduced. Let's define a *sith lord* to be one named Darth *something* from a medium containing the words *Star Wars*
3. Unique list of *Harry Potter* books - only return medium and year (as a value tuple). 
4. List of wizard names grouped by author in reverse order by author name.

Each method *must* be implemented twice - once using only *extension methods* and once using as much *LINQ* as possible.

#### Notes
You should use a constructor in the `QueriesTests` class to load a set (into a private field) of at least 10 wizards of your choosing using the object- and collection initializer notation, which can be used in your tests.

## Submitting the assignment

To submit the assignment you need to create a .pdf document using LaTeX containing the answers to the questions and a link to a public repository containing your fork of the completed code.
Upload the document to Peergrade.
