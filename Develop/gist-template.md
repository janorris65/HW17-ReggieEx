# Matching an URL with RegEx

It is just garble? the endless strings of seemingly random widgets and wingdings somehow bring me my morning interet gossip. Well, yes and no. Though, they do have a great variety to them. Its not all silly gibberish as a RegEx is able to be set to determine if a url is valid. 
Curious,  /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.
The URL matching validation statement uses the RegEx 
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
This is an, at most once anchored with string of 'http' followed possibly by 's'and : by two literal //. Any single digit, any letter, then . - as many times as possible.  Then 2-6 times matching any letter. Then Any amount of / word / . - Any amount of times ending with a /, if at all.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors like ^ and $, define a necessary "start" and "end" of an expression. Without these, the search will return any string that matches the other given parameters without a necessary beginning and end. 

In this case the string in question must begin with the 'http' and end with '/'

### Quantifiers

Quantifiers count and are placed after the counted parameters. * is zero or more (any amount); + is one or more (greater than zero); ? is zero or one (at most once); {} with numbers like {2}, mean matching 2 times. {} like {2,6} mean matching 2 to 6 times (greedily).

In this case At most one 's', At most one 'http', greater than 0 of letters or numbers, 2-6 letters, and any amount of letters, numbers with /'s. 

### OR Operator

(x|y) or [] represent OR statments that a string can contain OR selections of the contents. The two examples given differ in the previous captures those values while the latter, the square brackets just perform the function.

In this case, there are three OR groupings. One matching a greater than zero amount; Another matching 2-6; Another any amount.

### Character Classes

\d corresponds to a digit 0-9. \w corresponds to an a-z,A-Z,0-9, and _, \s is for spaces.

In this case, there are \d and \w in the OR groupings, letting these be pertinent matches in the OR groups.

### Flags

g, for global. m for multi line. and i for insensitive are flags found after the limiting / lines.
g will return as many results that fit and not stop at the first. m will match a start and end of a line not just a string. i will make the search case insensitive.

In this case nothing is called as this is written as a validation statement, so not a text search. 

### Grouping and Capturing

() will group components together to be searched for or have a quantifier applied to them. They also  return or capture these values for programming purposes. 

In this case, all search groups are grouped and captured together. (https?:\/\/) ([\da-z\.-]+)([a-z\.]{2,6}) ([\/\w \.-]*)

### Bracket Expressions

[] are OR statements of the values inside. Matching any items that can be found in the contained parameters with the given quantifiers.

In this case [\da-z\.-], [a-z\.], and [\/\w \.-]

### Greedy and Lazy Match

+ * {} are greedy quantifiers, as they will match as much as they can of their parameters. 
Adding a ? inside brackets with +* can make them lazy; they will match the smallest amount they can. 

In this case, these groupings are greedy; ([\da-z\.-]+)([a-z\.]{2,6}) ([\/\w \.-]*)

### Boundaries

\b or \B assert boundaries around a string for a word like \babc\b looks are the word 'abc'.

In this case there are none of these. 

### Back-references

\1 or \2.... will match further groupings based upon what the first grouping or second..... found.

In this case there are none of there.

### Look-ahead and Look-behind

(?=) and (?<=) looks for sequence in searches. d(?=r) looks for d only if followed by r and (?<=r)d looks for d only if preceded by r.

In this case there are none of these. 

## Author

My name is Joshua Norris. I like to write about interesting things like RegEx statement because to try is a step in learning. My github is https://github.com/janorris65. 