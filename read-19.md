## Python RegEx

`re` needs to be imported for RegEx to work.
compile()
search()
findall()
sub()
split()
match() return match object if text matches pattern. Else return None.
special characters can be read as part of the string if the string is prefixed with an r as follows: print(r"str\'n'g") prints str\'n'g instead of strn'g.
. - Matches any character.
^ - Matches the start of a string.
$ - Matches the end of a string.
[abc] - Matches a b or c (or whatever other characters are between the brackets).
[a-zA-z0-9] - Matches any letter or number regardles of capitalization.
\ - Can be used in front of metacharacters to turn them into regular characters to match. It can also be read as a normal backslash if there is a no recognized escape character after it.
\w - Matches any single letter/digit/underscore.
\W - Matches any character except \w.
\s - Matches one space/tab/newline.
\S - Matches any character except \s.
\d - Matches decimal digit 0-9.
\D - Matches any non-decimal digit.
\t - Matches tab.
\n - Matches newline.
\r - Matches return.
\A - Matches Starts of new lines.
\Z - Matches end of string.
\b - Matches only beginning or end of word.
+ - Matches all repetitions of a preceding character. GREEDY
* - CHECKS if a character appears 0+times (regex won't fail if it's not there). GREEDY
? - Checks if a preceding character appears exactly 0-1 times.
{x} - Repeat exactly x times.
{x, } - Repeat at least x times.
{x, y} - Repeat at least x times but not more than y.
() - Using these around a set of regex commands turns the resulting match into a 'group'. Multiple groups can be used as part of the same string in the same match on the same line (`(r'([\w\.-]+)@([\w\.-]+)'`).
group() - Matches the entire string with groups in it. Adding a number between the parens Matches that group starting from 1 not 0.