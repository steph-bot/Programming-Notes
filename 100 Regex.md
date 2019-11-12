## Regex

https://regexone.com

Match	abc123xyz	    Success

Match	define "123"	Success

Match	var g = 123;	Success

Regex: 123

```
const regex = /(\d+)\s+(\d+\.\d+\.\d+\.\d+\W\d+)\s+(\S+)?\s+(\d+\.\d+\.\d+\.\d+\W\d+)?/;
// groups with question marks are optional

const capturedGroups = string.match(regex);
if (capturedGroups) {
        const firstMatch = capturedGroups[1];
        const secondMatch = capturedGroups[2];
        const thirdMatch = capturedGroups[3];
        const fourthMatch = capturedGroups[4];
        }
        
        
        


abc…	Letters
123…	Digits
\d	Any Digit
\D	Any Non-digit character
.	Any Character
\.	Period
[abc]	Only a, b, or c
[^abc]	Not a, b, nor c
[a-z]	Characters a to z
[0-9]	Numbers 0 to 9
\w	Any Alphanumeric character
\W	Any Non-alphanumeric character
{m}	m Repetitions
{m,n}	m to n Repetitions
*	Zero or more repetitions
+	One or more repetitions
?	Optional character
\s	Any Whitespace
\S	Any Non-whitespace character
^…$	Starts and ends
(…)	Capture Group
(a(bc))	Capture Sub-group
(.*)	Capture all
(abc|def)	Matches abc or def```
