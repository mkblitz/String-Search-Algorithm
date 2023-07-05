# String Search Algorithm
String search algorithm I came up with which performs well, often beating benchmarks. Takes advantage of the PATTERN letter least found in the TEXT.

## Algorithm Outline
In general, we use string search algorithms when we're given a TEXT of length n, and a PATTERN of length m, and we want to find every instance of the pattern in the text, ideally in an eficiant manner.

The basic idea of this algorithm is as follows: first, you make a set of all the unique letters in your pattern <O(m)>, you then run through the text once <O(n)>, making a letter dictionary of lists of indices of any characters that are found in the PATTERN, as follows:

![image](https://github.com/mkblitz/String-Search-Algorithm/assets/47316278/1330a47a-e7db-46dd-94b3-ae89c3d78261)

Then, you find the letter from the PATTERN that shows up the fewest number of times in the TEXT <O(unique(m))>, and  you compare the PATTERN to the TEXT only at those indices from the list (in our example, the letter 'n' only shows up in the TEXT twice, at index 12 and index 16, as seen in the letter dictionary).

![image](https://github.com/mkblitz/String-Search-Algorithm/assets/47316278/76f7088c-14b1-46c2-910c-b63fababdd7b)

And then 

![image](https://github.com/mkblitz/String-Search-Algorithm/assets/47316278/ba68dde3-95dd-49a9-9853-4cacc762856c)

In this way we take advantage of the fact that in most patterns, there will be a letter that will show up in the text fewer times than the first letter, and we'll therefore only need to be comparing the pattern to the text as the number that that letter shows up in the text.
