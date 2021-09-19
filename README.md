# Here's a regex cheatsheet
🔤 A Python Regular Expressions Cheatsheet (import re)

### Show only all uppercase letters
```
    re.findall('[A-Z]', text)
```
### Show only all lowercase letters
```
    re.findall('[a-z]', text)
```
### Show all letters
```
    re.findall('[a-zA-Z]', text)
```
### Show all non-escaped characters
```
    re.findall('[^\\\\]', text)
```
### Show all numbers
```
    re.findall('[0-9]', text)
```
### Show all spaces
```
    re.findall('\s', text)
```
### Match a pattern a single time
```
    re.search('[0-9]{1}',text)
```
### Match a pattern at least once
```
    re.search('[0-9]+',text)
```
### Match a pattern zero or more times
```
    re.search('[0-9]*',text)
```
### Match a pattern one or more times
```
    re.search('[0-9]+',text)
```
### Show all punctuation
```
    re.findall('[^a-zA-Z0-9]', text)
```
### Match any character
    ```
    re.findall('.(#)', text)
    ```
### Match any digit
```
    re.findall('\d', text)
```
### Match any whitespace
```
    re.findall(r'\s', text)
```
### Match any character not in a list
```
    re.findall('[^aeiouAEIOU]', text)
```
### Match a word boundary
```
    re.findall(r'\b\w', text)
```
### Match a non-word boundary
```
    re.findall(r'\B\w', text)
```
### Match a digit
```
    re.findall(r'\d', text)
```
### Match any alphanumeric character
```
    re.findall(r'\w', text)
```
### Match any non-alphanumeric character
```
    re.findall(r'\W', text)
```
### Match any uppercase character
```
    re.findall(r'\u', text)
```
### Match anything other than an uppercase character
```
    re.findall(r'\l', text)
```
### Match any whitespace character
```
    re.findall(r'\s', text)
```
### Match anything other than a whitespace character
```
    re.findall(r'\S', text)
```
### Match a word
```
    re.findall(r'\w', text)
```
### Match a non-word
```
    re.findall(r'\W', text)
```
### Match a newline
```
    re.findall(r'\n', text)
```
### Match a carriage return
```
    re.findall(r'\r', text)
```
### Remove all the lines containing 'Fig {number}.{number}'
```
    re.sub(r'Fig (\d+).(\d+)', '', text)
```
### Replace 'Fig {number}.{number}' with 'Figure {number}.{number}'
```
    re.sub(r'Fig (\d+).(\d+)', 'Figure \g<1>.\g<2>', text)
```
### Find all the page numbers
```
    re.findall(r'\d+(?!\.)', text)
```
### Find all the percentages
```
    re.findall(r'\d+%', text)
```
### Find all the chapters
```
    re.findall(r'Chap\b', text)
```
### Find all the numbers in a name
```
    re.findall(r'\d+\b', text)
```
### Find all the words
```
    p = re.findall(r'[A-Z][a-z]+\b', text)
```
### Find all the words, not at the start of a paragraph
```
    p = re.findall(r'\b[A-Z][a-z]+\b', text)
```
### Find all the words, not at the start of a chapter
```
    p = re.findall(r'\b[A-Z][a-z]+\b', text)
```
### Find all the words, not at the start of a chapter
```
    p = re.findall(r'\b[A-Z][A-Za-z]*\b', text)
```
### Split the text on chapter
```
    p = re.split(r'Chap\b', text)
```
### Split the text on chapter, then sentence
```
    p = re.split(r'Chap\b', text)
    p = re.split(r'\.', p[1])
```
### Break the text into lines
```
    p = re.split(r'\\n', text)
```
### Split the text on sentence
```
    p = re.split(r'\n', text)
```
### Split the text on line
```
    p = re.split(r'\\n', text)
```
### Split the text on letter
```
    p = re.split(r'\\?\w', text)
```
### Remove all non-ascii characters
```
    re.sub(r'[^\x00-\x7F]', '', text)
```
### Remove all punctuation
```
    re.sub(r'[^\w\s]', '', text)
```
### Making this List
```
turning this:
#Show only all uppercase letters
    re.findall('[A-Z]', text)

into this:
###Show only all uppercase letters
    ```
    re.findall('[A-Z]', text)
    ```

import re
text= r'''#Show only all uppercase letters\n    re.findall('[A-Z]', text)'''
text= re.sub(r'^#([^\n]*)\n([^#]*)', r'###\1\n```\n\2```',text, flags=re.M)
print(text)

```
