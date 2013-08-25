# Foswig.js

A Javascript library which allows you to easily create [Markov chains](http://en.wikipedia.org/wiki/Markov_chain) based on arbitrary dictionaries in order to create readable pseudo random words (Yes the name was generated by the library). See a demo of this library in action [here](http://mrsharpoblunto.github.io/foswig.js/)

## Usage

```Javascript


// Create the markov chain and specify the Order of the markov chain.
// The order (an integer > 0) indicates how many previous letters are 
// taken into account when selecting the next. A smaller order will
// result in more randomized less recognizeable output. Conversely a
// higher order will result in words which resemble more closely those
// in the original dictionary.
var chain = new foswig.MarkovChain(3);

// add words into the markov chain one at a time
chain.addWordToChain("random");

//OR add all the words in an array at once
var dictionary = ["hello","foswig"];
chain.addWordsToChain(dictionary);
  
// generate a random word with a minimum of 5 characters, a maximum of 10 letters, 
// and that cannot be a match to any of the input dictionaries words
var randomWord = chain.generateWord(5,10,false);
```

## License

Foswig.js is licensed under the [MIT license](https://github.com/mrsharpoblunto/foswig.js/blob/master/LICENSE).
