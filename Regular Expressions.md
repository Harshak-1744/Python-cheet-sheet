# Understanding Regular Expressions (Regex)

Regular expressions, or regex for short, are like magic words that help you find specific things in text. It's like finding a treasure in a sea of words.

## Literal Characters

Literal characters are simple; they are just regular letters and numbers that match exactly what they look like.

**Example:**

Imagine you're searching for the word "cat" in a sentence. You type "cat" as your magic word, and if the sentence contains "cat," you'll find it!

```python
import re

text = "I have a cat and a hat."
pattern = "cat"
match = re.search(pattern, text)
if match:
    print("Found:", match.group())
```
**Result:**
```
Found: cat
```

## Metacharacters

### Dot (.)

The dot `.` can match any character except a new line.

**Example:**

If you use `a.b` as your magic word, it will find any three-letter word where the middle letter is anything.

```python
import re

text = "axb, aab, a1b, a#b"
pattern = "a.b"
matches = re.findall(pattern, text)
print("Matches:", matches)
```

**Result:**
```
Matches: ['axb', 'aab', 'a1b']
```

### Asterisk (*)

The asterisk `*` matches characters as many times as they appear, including zero times.

**Example:**

If you use `ab*c` as your magic word, it will find any word starting with "a" and ending with "c," with zero or more "b" characters in between.

```python
import re

text = "ac, abc, abbc, abbbc"
pattern = "ab*c"
matches = re.findall(pattern, text)
print("Matches:", matches)
```

**Result:**
```
Matches: ['ac', 'abc', 'abbc', 'abbbc']
```

### Plus (+)

The plus `+` matches characters one or more times.

**Example:**

If you use `ab+c` as your magic word, it will find any word starting with "a" and ending with "c," with at least one "b" character in between.

```python
import re

text = "ac, abc, abbc, abbbc"
pattern = "ab+c"
matches = re.findall(pattern, text)
print("Matches:", matches)
```

**Result:**
```
Matches: ['abc', 'abbc', 'abbbc']
```

### Question Mark (?)

The question mark `?` matches a character only once or not at all.

**Example:**

If you use `ab?c` as your magic word, it will find any word starting with "a" and ending with "c," with zero or one "b" character in between.

```python
import re

text = "ac, abc, abbc"
pattern = "ab?c"
matches = re.findall(pattern, text)
print("Matches:", matches)
```

**Result:**
```
Matches: ['ac', 'abc']
```

### Pipe (|)

The pipe `|` acts like an OR operator, helping you find one thing or another.

**Example:**

If you use `apple|banana` as your magic word, it will find either "apple" or "banana" in a sentence.

```python
import re

text = "I like apple pie and banana smoothies."
pattern = "apple|banana"
matches = re.findall(pattern, text)
print("Matches:", matches)
```

**Result:**
```
Matches: ['apple', 'banana']
```

### Character Classes ([])

Character classes let you find a character from a set of characters.

**Example:**

If you use `[aeiou]` as your magic word, it will find any vowel (a, e, i, o, or u) in a sentence.

```python
import re

text = "I have an apple and an orange."
pattern = "[aeiou]"
matches = re.findall(pattern, text)
print("Matches:", matches)
```

**Result:**
```
Matches: ['a', 'e', 'a', 'e', 'a', 'o', 'a', 'e', 'o', 'a', 'e']
```

### Grouping (())

Grouping helps you apply the magic to a group of characters.

**Example:**

If you use `(ab)+` as your magic word, it will find one or more occurrences of "ab" in a word.

```python
import re

text = "ab, abab, ababab"
pattern = "(ab)+"
matches = re.findall(pattern, text)
print("Matches:", matches)
```

**Result:**
```
Matches: ['ab', 'abab', 'ababab']
```

### Curly Braces ({})

Curly braces help you find an exact number of characters.

**Example:**

If you use `a{2}` as your magic word, it will find exactly two "a" characters in a word.

```python
import re

text = "I have two apples."
pattern = "a{2}"
matches = re.findall(pattern, text)
print("Matches:", matches)
```

**Result:**
```
Matches: ['aa']
```
