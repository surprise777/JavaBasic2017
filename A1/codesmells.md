# Markdown

Markdown is a plain-text file format. There are lots of programming tools that use Markdown, and it's useful and
easy to learn. Hash marks (the number sign) indicate headers. Asterisks indicate lists.

# Template

Use the following Code Smell template (copy and paste it at the end of this file and then edit it; don't include the "Begin template" or "End template" lines):

==== Begin template ====
## Code Smell: [Write the code smell name]

### Code Smell Category: [Write the code smell category name]

### List of classes and line numbers involved:

* [Write a class and list of line numbers, one class per asterisk, that describe the smell]

### Description:

[In your own words, explain how this particular code smells.]

### Solution:

[In your own words, explain how you might solve this code smell:
how would you refactor the code?]
==== End template ====

# List of code smells

## Code Smell: [Long Method]

### Code Smell Category: [Bloaters]

### List of classes and line numbers involved:

* [WarehouseSimulation.start(WarehouseSimulation.java: 41)]

### Description:

[A method WarehouseSimulation.start is expected to write within 10 lines. which make the code hard to trace. ]

### Solution:

[Looking through the method start, too many if statements ("Order","Picker", "Sequencer"), so decompose the
conditional, extract each condition to boolean functions(Line 52-64 to isOrder(), Line 65-77 to isPicker(), etc)then
call them. ]

## Code Smell: [Large Class]

### Code Smell Category: [Bloaters]

### List of classes and line numbers involved:

* [WarehouseManager(WarehouseManager.java:13)]

### Description:

[There are 19 similar attributes and methods in the WarehouseManager class, making the class large, complicated to use]

### Solution:

[Looking through the WarehouseManager class, many attributes have similar ways of functioning while different type,
which can be extracted as some subclass, and construct the original WarehouseManager as interface or abstract class]

## Code Smell: [Dead Code]

### Code Smell Category: [Dispensables]

### List of classes and line numbers involved:

* [Worker(Worker.java:3)]

### Description:

[This class has never been used, comparing with Picker and Sequencer. ]

### Solution:

[From WarehouseSimulation.java we could see workers are specific to pickers and sequencers or scan events, so Worker
class can be constructed to abstract class and modify Picker and Sequencer to its subclass, or delete this class. ]

## Code Smell: [Alternative Classes With Different Interfaces]

### Code Smell Category: [Object Orientation Abusers]

### List of classes and line numbers involved:

* [OrderListManager(OrderListManager.java: 10) vs WarehouseManager(WarehouseManager.java: 13)]

### Description:

[Firstly, we can see OrderListManager class is not used. Besides most method like addOrders have similar functions with
  WarehouseManager class, even WarehouseManager does the work more specifically(divided into picker and sequencer). ]

### Solution:

[OrderListManager.java can be deleted, or make OrderListManager class as super class of WarehouseManager.]
