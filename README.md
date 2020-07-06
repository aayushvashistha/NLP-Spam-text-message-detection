# Natural Language Processing for Text Classification with NLTK and Scikit-learn

## Background
In this project of Natural Language Processing in Python, I used basics of tokenizing, part of speech tagging, stemming, chunking, and named entity recognition followed by Machine Learning and text classifications using simple support vector classifier. To improve text classification results I used:
 * Regular Expressions
 * Feature Engineering 
 * Multiple scikit-learn Classifiers
 * Ensemble Methods

## Data Source
This dataset has been taken from UCI Machine Learning Repository. Data originally fetched  from the Grumbletext Web site.. UCI Machine Learning Repository URL: https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection#
It contains over 5000 SMS labeled messages that have been collected for mobile phone spam research.

## Preprocess the Data
Preprocessing the data is an important step in natural language process. I will convert our class labels to binary values using the LabelEncoder from sklearn, replace email addresses, URLs, phone numbers, and other symbols by using regular expressions, remove stop words, and extract word stems.

### Regular Expression
A RegEx, or Regular Expression, is a sequence of characters that forms a search pattern.

Some common regular expression metacharacters - copied from wikipedia

^ Matches the starting position within the string. In line-based tools, it matches the starting position of any line.

. Matches any single character (many applications exclude newlines, and exactly which characters are considered newlines is flavor-, character-encoding-, and platform-specific, but it is safe to assume that the line feed character is included). Within POSIX bracket expressions, the dot character matches a literal dot. For example, a.c matches "abc", etc., but [a.c] matches only "a", ".", or "c".

[ ] A bracket expression. Matches a single character that is contained within the brackets. For example, [abc] matches "a", "b", or "c". [a-z] specifies a range which matches any lowercase letter from "a" to "z". These forms can be mixed: [abcx-z] matches "a", "b", "c", "x", "y", or "z", as does [a-cx-z]. The - character is treated as a literal character if it is the last or the first (after the ^, if present) character within the brackets: [abc-], [-abc]. Note that backslash escapes are not allowed. The ] character can be included in a bracket expression if it is the first (after the ^) character: []abc].

[^ ] Matches a single character that is not contained within the brackets. For example, [^abc] matches any character other than "a", "b", or "c". [^a-z] matches any single character that is not a lowercase letter from "a" to "z". Likewise, literal characters and ranges can be mixed.

$ Matches the ending position of the string or the position just before a string-ending newline. In line-based tools, it matches the ending position of any line.

( ) Defines a marked subexpression. The string matched within the parentheses can be recalled later (see the next entry, \n). A marked subexpression is also called a block or capturing group. BRE mode requires ( ).

\n Matches what the nth marked subexpression matched, where n is a digit from 1 to 9. This construct is vaguely defined in the POSIX.2 standard. Some tools allow referencing more than nine capturing groups.

* Matches the preceding element zero or more times. For example, abc matches "ac", "abc", "abbbc", etc. [xyz] matches "", "x", "y", "z", "zx", "zyx", "xyzzy", and so on. (ab)* matches "", "ab", "abab", "ababab", and so on.

{m,n} Matches the preceding element at least m and not more than n times. For example, a{3,5} matches only "aaa", "aaaa", and "aaaaa". This is not found in a few older instances of regexes. BRE mode requires {m,n}.

## Generating Features
To create features of Machine Learning Algorithms, feature engineering is used, which is the process of using domain knowledge of data. In this project, features are the words in each text message. For this purpose, it is necessary to tokenize each word. I have used the 1500 most common words as features.

## Scikit-Learn Classifiers with NLTK
With dataset, I built algorithms! Let's start with a simple linear support vector classifier, then expand to other algorithms. I have imported each algorithm by using sklearn library along with some performance metrics, such as accuracy_score and classification_report.
