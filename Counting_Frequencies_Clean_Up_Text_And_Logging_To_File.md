# Modern Python Standard Library Cookbook: Counting Frequencies, Clean Up Text, and Logging To File

I'm glad to learn a technique for counting elements in an iterable like a list of words with code like the following. I appreciate being introduced to some of the methods of class `Counter`.

```
txt = "This is a vast world you can't traverse world in a day"
from collections import Counter
the_counter_which_contains_a_dictionary_of_elements_and_counts = Counter(txt.split())
```

I find it very valuable to have a technique for removing common punctuation characters. See documentation for `maketrans` at https://docs.python.org/3.3/library/stdtypes.html?highlight=maketrans#str.maketrans.

```
import string
trans = str.maketrans('', '', string.punctuation)
txt = txt.lower().translate(trans)
```

I find it valuable to learn an idiom for logging involving configuring a logger in a module that is run, allowing importing a function that uses a logger, and running that function if a module is run. Perhaps consider ChatGPT 4o's answer to the question, "How do I log in a Python package with one module with a main entry point, one or more other modules, and test modules?".