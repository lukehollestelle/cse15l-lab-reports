**Lab Report 5 for week 10:**
## Luke Hollestelle

---
I used `diff` to find the differences between the two files.  My result.txt file had all of the result for joe's version of markdown parse, while my another-result.txt had all of the results for mine.  

The first test that had different outputs was testfile 14.  This file contains the following:
```
`Foo
----
`

<a title="a lot
---
of dashes"/>
```
Joe's version of MarkdownParse is correct in this situation.  My current version of MarkdownParse still has print methods within it, which print out the current index after an iteration of one of the loops.  This was to help me debug it at first, but it is now causing errors because it is printing out extra information.  The obvious solution to this would be to remove the print statements.

The second text case that I found was different was testfile 201.  This file includes the following text:
```
[foo]: <bar>(baz)

[foo]
```

Joe's implementation is also correct here.  This is tricky because it has characters in between the brackets and the parenthesis.  Adding an if statement that checks if the character after the closed bracket is the open parenthesis would solve this issue.  