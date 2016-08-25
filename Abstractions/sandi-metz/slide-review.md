# Part 1: Refactoring Concepts

## Introduction

* This talk is about Martin Fowler and Kent Beck's chapter in *Refactoring - Improving The Design of Existing Code*
* The joke of the whole talk is its Sandi Metz's book report on the chapter

## Classic Code Smells

* Alternative Classes w/ Different Interfaces
* ~~Comments~~
* Data Class
* Data Clumps
* Divergent Change
* Duplicated Code
* Feature Envy
* Inappropriate Intimacy
* ~~Incomplete Library Client~~
* Large Class
* Lazy Class
* Long Method
* Long Parameter List
* Message Changes
* Middle Max
* Parallel Inheritance Hierarchies
* Primitive Obsession
* Refused Bequest
* Shotgun Surgery
* Speculative Generality
* Switch Statements
* Temporary Field


### Bloaters

* Long Method
* Large Class
* Data Clumps
* Long Parameter List
* Primitive Obsession

### Tool Abusers

* Switch Statements
* Refused Bequest
* Alternative Classes w/ Different Interfaces
* Temporary Field

### Change Preventers

* Divergent Change
* Shotgun Surgery
* Parallel Inheritance Hierarchies

### Dispensibles

* Lazy Class
* Speculative Generality
* Data Class
* Duplicated Code

### Couplers

* Feature Envy
* Inappropriate Intimacy
* Message Chains
* Middle Man

## Refactoring Recipe

#### From the book here:

1. Decide how to split the responsibilities of the class
  * If the responsibilities of the old class no longer match its name, rename the old class
2. Create a new class to express the split-off responsibilities
3. Make a link from the old to the new class
  * You may need at two-way link. But don't make the back link until you find you need it.
4. Use Move Field on each field you want to move
5. Test after each move
6. Use Move Method to move methods over from old to new. Start with lower-level methods (rather than calling) and build to the higher level.
7. Test after each move.
8. Review and reduce the interfaces of each class

### Perspective on Data Clumps

> Data clumps are bunches of data that hang around together and really out to be made
into their own object. A good test is to consider deleting one of those data values: If you did this, would the others make any sense? If they don't its a sure sign that you have
and objects that's dying to be born.

Steps to this:

1. Extract Class
2. Preserve Whole object
3. Introduce Parameter Object

[Resource For This](http://www.industriallogic.com/wp-content/uploads/2005/09/smellstorefactorings.pdf)

# Time For Some Code
