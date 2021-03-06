# OcuCount
A tiny NodeJS module to perform wordcounts on single or arrays of strings.

[![npm](https://img.shields.io/npm/v/ocucount.svg?style=flat-square)](https://www.npmjs.com/package/ocucount)
[![npm](https://img.shields.io/npm/dt/ocucount.svg?style=flat-square)](https://www.npmjs.com/package/ocucount)

#Installation
Installation is very simple due to OcuCount being on NPM. Simply type: `npm install ocucount` from a console in the project directory then add `var ocucount = require('ocucount');` to the top of your project file.

#Usage
Usage of OcuCount is fairly simple. It has as few functions as possible to keep the size down and ease of use high.

##For a single strings
For single strings simply use the following function:
```javascript
var wordcount = ocucount.count('What are you doing my friend? you are a good friend');
```
Simply replace the test string with the string you want to perform the wordcount on. In this example, wordcount would be the following:
```javascript
[
    word { word: 'what', count: 1 },
    word { word: 'are', count: 2 },
    word { word: 'you', count: 2 },
    word { word: 'doing', count: 1 },
    word { word: 'my', count: 1 },
    word { word: 'friend', count: 2 },
    word { word: 'a', count: 1 },
    word { word: 'good', count: 1 } 
]

```

##For multiple strings
OcuCount can also be used on arrays of stings. For example:
```javascript
var wordcount = ocucount.count(['What are you doing my friend?','You are a good friend.','But I love you!']);
```
In this example, wordcount would be:
```javascript
[
    word { word: 'what', count: 1 },
    word { word: 'are', count: 2 },
    word { word: 'you', count: 3 },
    word { word: 'doing', count: 1 },
    word { word: 'my', count: 1 },
    word { word: 'friend', count: 2 },
    word { word: 'a', count: 1 },
    word { word: 'good', count: 1 },
    word { word: 'but', count: 1 },
    word { word: 'i', count: 1 },
    word { word: 'love', count: 1 }
]
```

##Sorting Ocucount word lists
Ocucount does not default to sorting your lists of words. To do that, simply call the following:
```javascript
//create an OcuCount word list
var wordcount = ocucount.count(['What are you doing my friend?','You are a good friend.','But I love you!']);
//sort it
wordcount = ocucount.sortWords(wordcount);
```
This will return the list generated by the other main Ocucount function but sorted from lowest to highest usage.

---

[![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat-square)](https://github.com/vandie/OcuCount/blob/master/LICENSE)

---

Follow me on twitter ([@MVD_Vandie](https://twitter.com/MVD_Vandie)) or on github in order to keep track of my projects and releases.

[![Twitter Follow](https://img.shields.io/twitter/follow/mvd_vandie.svg?label=Follow%20on%20Twitter&style=flat-square)](https://twitter.com/MVD_Vandie) 
[![GitHub followers](https://img.shields.io/github/followers/vandie.svg?label=Follow%20on%20Github&style=flat-square)](https://github.com/vandie)

Enjoy. :D