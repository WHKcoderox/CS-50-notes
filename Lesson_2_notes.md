[err1]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-2-at-7m10s.png "Did not include required header file"
[duck]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-2-at-31m21s.png "Quack"
[strings]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-2-at-1h22m5s.png "Strings"
[iterable]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-2-at-58m31s.png "Iterating through string"
[argcv]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-2-at-1h28m48s.png "argcv"


# Video Lesson 2 Notes

### 'Debugging' - Hell
- Takeaways: become those anti-social freaks behind the computer screen tapping away with your fingers and chatting away with yourself :)
- Run through code, check the error logs, take note of terms you understand and keep them in mind.
- Basically, be okay with screwing up.
Perhaps one example:
![Err1][err1]
In this example, upon reading certain parts of what the console is basically yelling at you, you might recognise certain things like 'implicitly declaring' and 'library function' and of course the source of your error, 'printf'. From there you proceed to understand the erro which is just you forgetting to do this:
```C
#include <stdio.h>
```
Cheerio!
And here's how much embarrassment you should be ready to embrace:
![Duck][duck]

### 'Problem Sets Overview' - Aims of a Good Programmer
1. Scope: Always make sure the code is **purposeful**. You may ask yourself, "What exactly is my code going to solve?"
2. Correctness: A no-brainer, the code has to actually serve its purpose at the end of the day. Note that this does not include how successful it is, only the fact that your code manages to give expected outputs (may not be in the expected time :P)
3. Design: The code's inner workings: Is it optimised? Is it good enough for the problem it solves? Is the logic design efficient? Elegant?
4. Style: Make your code readable, maintainable and generally unmessy.
5. Integrity: Don't lie to yourself. Coding is as real as the real world gets - and without enough privileges you can't have room for cheating by then. Learn to handle things honestly and earnestly first, then let your hands be dirtied, but only when you're prepared for the circumstances.

### 'Secret-key Cryptography' - Very Basic, Very Vulnerable Cryptography
- A key is used to generate some cryptic string for the input string and thus makes it impossible to understand by reading it. Of course, then you just need the same key, same cryptic string and the encryption algorithm in order to undo the generation and obtain the original, and hopefully readable string. Not recommended for any serious developments, this cryptography is very weak given that the key is hard to hide from hackers. 

### 'Strings', 'ascii', 'Capitalise', 'argv' - Iterables and Command Line Arguments
- Strings are immutable (read-only) chains of characters that are terminated by the '\0' character (in binary it's just 00000000). An example of how some strings might be stored:
![Strings][strings]
- And you can read every character just fine with the use of a for loop, by pointing at every single letter inside the string.
![Iterable][iterable]
```C
#include <stdio.h>
#include <string.h>

//iterating through strings
int main(){
  char str[100]; // because strings. max length is 100.
  gets(str);     // from stdin or standard input
  
  for(int i = 0, n = strlen(str); i < n; i++){ //!IMPORTANT: don't overuse the function to count the length of the string; it is not a property of the string and thus will effect unnecessary operations. 
    // multiple initialisation of variables of the same type works, i.e. char c, b='b', a; also works
    // do whatever here i.e. printf("%c", str[i]);
  }
}
```
- Btw, did you know that your main function can return completion and error codes to the console? Just check what it was with the command (after running your code of course)
```.sh
~/directory $ echo $?
```
- One last thing, here's a way that you can incorporate command line arguments into your code! Just accept the arguments ```argc``` and ```argv[]``` and you'll accept *argc* as the *count* of arguments passed and *argv* as the *vector* (or dynamically sized array) of arguments passed as strings. Of course the "argc argv" thing is just naming convention and just for clarity. Here's an example of the code!
![Argcv][argcv]
More on argc and argv here without cs50 hax: https://stackoverflow.com/questions/3898021/regarding-mainint-argc-char-argv
- I can plus one to a char too :) check it out
```C
#include <stdio.h>

int main(int argc, char* argv[]){ // these won't be used here, but char** is (char*)* where each * is a pointer which likely is to an array. 
  for(int i = 65; i < 65 + 26; i++){
    // you can choose to explicitly typecast i to a char, or just leave it in its numerical value and allow the %c placeholder
    // to effect an implicit conversion for you, as shown below. 
    printf("%i is %c is %c.\n", i, i, (char) i);
  }
  
  // or, you can also iterate from a-z or A-Z. Same thing with the implicit explicit conversions.
  for(char c='A'; c <= 'Z'; c++){
    // c++ :)
    printf("%c is %i is %i.\n", c, c, (int) c);
  }
}
```

### The End



