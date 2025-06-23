# Day 2: Word Frequency Analyzer

## Task
Write a function that takes a paragraph and returns a dictionary of word frequencies (case-insensitive, punctuation removed).

---

## Python Code
```python
def word_freq(text):
    frequency = {}
    text = text.lower().replace('.', '').strip()
    words = text.split()
    for word in words:
        if word in frequency:
            frequency[word] += 1
        else:
            frequency[word] = 1
    return frequency

text = "Python is great. Python is easy to learn. Great things take time."
print(word_freq(text))
```

### Without `.split()` and `.replace()`
```python
def words(text):
    text = text.lower()
    word = []
    Text = ''
    for i in text:
        if i != ' ' and i != '.':
            Text += i
        elif i == '.':
            pass
        else:
            word.append(Text)
            Text = ''
            
    word.append(Text)
    return word

def words_freq(text):
    word = words(text)
    frequency = {}
    for i in word:
        if i in frequency:
            frequency[i] += 1
        else:
            frequency[i] = 1
    return frequency

text = "Python is great. Python is easy to learn. Great things take time."
print(words_freq(text))
```

## Output
```python
{'python': 2, 'is': 2, 'great': 2, 'easy': 1, 'to': 1, 'learn': 1, 'things': 1, 'take': 1, 'time': 1}
```

---

## Explanation of Code
- The function converts all text to lowercase and removes periods to normalize the input.
- It splits the text into individual words using `.split()` or manually.
- A dictionary is used to count how many times each word appears.
- If a word is already in the dictionary, we increment its count. If not, we add it with a count of 1.
- Finally, the function returns the dictionary of word frequencies.

---

## What I Learned
- How to clean and normalize text for analysis  
- How to use dictionaries for counting  
- How to simulate `.split()` and `.replace()` manually using loops and conditionals
