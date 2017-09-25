[ptr1]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-4-at-6m34s.png "pointers 1"
[ptr2]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-4-at-10m1s.png "pointers 2"
[malloc]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-4-at-37m20s.png "Malloc"


# Video Lesson 4

### 'Strings are a Lie' - Unravelling <cs50>'s Handholding
- Back to the 
```C
char**
char* argv[]
// or more specifically, the asterisk '*'
```
thing. To be aware of this is to be aware of what is being stored and how things are being stored. Generally, arrays aren't actual bundles of stuff nicely packaged for the coder and in actuality they are just pointers, or addresses, to the data in memory.

Here's some examples as to what happens if you don't account for this difference in address.
![P1][ptr1]
![P2][ptr2]
In the given examples, because the addresses are either being compared or the same address to a piece of data is used by two different variables, things may not work as expected (isolating changes where they share the common space or effecting changes on multiple adresses by only changing one or simply thinking of the string as a string - it's really just another address)

### 'Program Memory' - The Stack, Pointers and More
- Variables have lifetime scopes and always have some kind of address to them, since every variable has to be stored in memory somehow (then they will need some kind of postal code in case someone wants to take them away D:). To be careful about such differences will save your code from mistakes like attempting to manipulate data across different addresses by only changing the values at one, since the other variable won't be affected by the change.
- That's where pointers, denoted by the \*, exist to store the *addresses* of things. This is exactly what makes the low level versatile: by using addresses, I can simply point to the next element, and the next, and the one after, and simply use a square bracket ```[n]``` to denote how many elements after the first I would count, to return the resultant element at that specific spot.

### 'malloc' - Memory Allocation
- Special to C. As demonstrated below, it involves finding and reserving some memory and then returning its address which can be stored in a pointer, possibly to store a string of some sort.
![Malloc][malloc]
Here, the sizeof() is used in order to properly count the number of bytes per character so as to assign exactly that amount of memory for the char* pointer.

###




