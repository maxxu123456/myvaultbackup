Given a pattern, text: is pattern a substring of text?

X is a substring of y if all of the characters in x are present in the same order in y with no gaps.


n: length of text
m: length of pattern


Two types of pattern matching,

- Single Occurrence
- Multiple Occurrence

Brute Force
 - try every possible value
![[Pasted image 20240325141609.png]]

```python
def bruteforce(pattern,text):
	j = 0
	while j <=len(text)-len(pattern):
		k=0
		while k < len(pattern) and pattern[k] == text[j+k]:
			k+=1
		if k = len(pattern):
			#found
		else:
			# no luck
			j = j+1
```


Java string.contains() uses brute force since brute force for English text is efficient.

## How to improve Brute Force

Use Boyer-Moore Algorithm, Key Idea: use the text character that mismatched to decide how far to shift.

"Preprocessing" step. Only need the pattern, before looking at text.

Build last occurrence Table, track the location where each character appears for the last time in the pattern.
![[Pasted image 20240325143917.png]]


![[Pasted image 20240325144013.png]]

