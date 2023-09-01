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
| Metacharacter | Description |
| ------------- | ----------- |
| .           | Matches any letter or symbol, except a new line. It's like a detective's magnifying glass looking for anything. |
| *           | Matches the preceding letter or group many times or not at all. It's like saying "any amount, even zero." |
| +           | Matches the preceding letter or group at least once or more. It's like saying "at least one or more." |
| ?           | Matches the preceding letter or group once or not at all. It's like saying "Either one or zero." |
| []          | Helps you find a specific letter from a group of letters. It's like a treasure map with clues. |
| ()          | Group letters together so you can treat them as one. It's like putting items in a box. |
| {}          | Tells you exactly how many times a letter or group should appear. It's like counting how many candies you want. |
| OR          |	Helps you choose between two things. It's like picking your favorite ice cream flavor. |


# Understanding Regular Expression Functions

Regular expressions (regex) are like special tools for working with words and text. They help you do cool things with words, like finding them, changing them, and more!

## Find a Word in a Sentence (search)

Imagine you have a big storybook, and you want to find a specific word, like "cat," in the story. You read the book and stop when you find the word "cat." That's what `search` does.

## Check the Start of a Word (match)

Suppose you have a list of words, and you want to check if a word starts with a certain letter or letters, like "apple" or "banana." `match` helps you do that. If you see "apple" at the beginning of the word, you know it's a match.

## Find Many Words (findall)

Imagine you have a bunch of books, and you want to find all the words that are the same as "apple." `findall` helps you find all those words, and you can count them.

## Find and List Words (finditer)

This is similar to `findall`, but instead of giving you all the words at once, it gives you one word at a time. It's like finding one treasure after another in a treasure hunt.

## Change a Word (substitute - sub)

Suppose you have a sentence with a word you don't like, and you want to change it to something else. `sub` helps you do that. It's like changing "rainy" to "sunny" to make the day better.

These functions are like magic tools for words. They help you explore stories, find hidden treasures, and even make sentences better!


| Function                     | Description                                                                                                                                                  |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Find a Word in a Sentence** (`search`) | Imagine you have a big storybook, and you want to find a specific word, like "cat," in the story. You read the book and stop when you find the word "cat." That's what `search` does. |
| **Check the Start of a Word** (`match`) | Suppose you have a list of words, and you want to check if a word starts with a certain letter or letters, like "apple" or "banana." `match` helps you do that. If you see "apple" at the beginning of the word, you know it's a match. |
| **Find Many Words** (`findall`) | Imagine you have a bunch of books, and you want to find all the words that are the same as "apple." `findall` helps you find all those words, and you can count them. |
| **Find and List Words** (`finditer`) | This is similar to `findall`, but instead of giving you all the words at once, it gives you one word at a time. It's like finding one treasure after another in a treasure hunt. |
| **Change a Word** (`substitute - sub`) | Suppose you have a sentence with a word you don't like, and you want to change it to something else. `sub` helps you do that. It's like changing "rainy" to "sunny" to make the day better. |

