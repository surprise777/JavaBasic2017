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

[A method like WarehouseSimulation.start is expected to write within 10 lines. which make the code hard to trace. ]

### Solution:

[Looking through the method like start, too many conditional statements cause the long method, so decompose the
conditional, extract some condition to a new boolean function then call them. ]