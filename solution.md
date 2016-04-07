# Code-Wars-1-Reverse-Letters-in-Words

Write a function that takes in a string of one or more words, and returns the same string, but with all five or more letter words reversed (Just like the name of this Kata). Strings passed in will consist of only letters and spaces. Spaces will be included only when more than one word is present.


Examples:

spinWords( "Hey fellow warriors" ) => returns "Hey wollef sroirraw" 
spinWords( "This is a test") => returns "This is a test" 
spinWords( "This is another test" )=> returns "This is rehtona test"

SOLUTION:

function spinWords(arrayWords){
// since function is taking in a string argument, split the string into an array of words
    arrayWords = arrayWords.split(' ');
// loop through each word in array
// assign letters to the ith iteration of each word in which the for loop is looping through
    for(var i=0, letters; letters = arrayWords[i]; i++) {
 // if the length of letters in word is greater than 4, get that word and reverse all the letters.
        if(letters.length > 4) arrayWords[i] = letters.split('').reverse().join('');
    }
    return arrayWords.join(' ');
}
