# Video Lesson 1 Notes
[scratch main func]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-1-at-1m48s.png "Damnit Scratch"
[scratch while loops]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-1-at-3m35s.png "Scratch while true loops"
[scratch for loops]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-1-at-4m9s.png "Scratch for loops"
[scratch variables]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-1-at-4m50s.png "Scratch Variables"
[scratch boolean]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-1-at-6m3s.png "Scratch Booleans"
[scratch ifelse]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-1-at-7m21s.png "Scratch Conditioning"
[scratch arrs]: https://github.com/WHKcoderox/CS-50-notes/blob/master/images/Screenshot-2016-fall-lectures-1-at-8m50s.png "Scratch Arrays"

### 'Scratch vs. C', 'Loops', 'Arrays', 'Hello, C' - From Scratch to C
While true loops indirectly imply that there are more sophisticated terminating conditions to be handled within the loop body, and that the loop by default should not break.
Scratch:
![Scratch Main Function][scratch main func]
![Scratch Forever][scratch while loops]
![Scratch Repeat][scratch for loops]
![Scratch Variables][scratch variables]
![Scratch Boolean][scratch boolean]
![Scratch If-Else][scratch ifelse]
![Scratch Lists][scratch arrs]
___
C Syntax:
```C
#include <stdio.h> // including C's standard input/output library (stdio) as header file (holding all the declarations of emepty member funcs (abstract classes) which are defined i.e. coded elsewhere to make the code neat) 

int main (void) { // no arguments, the main function is the function that runs every time the file is executed

  while (true) {
    // while (true) loops
  }
  
  for (int i = 0; i < limit; i++){
    // for loops
  }
  
  printf("Hello World\n"); // formatted print, this prints Hello World followed by a newline character (\n)
  
  if (condition) {
    // if condition, do this
  }
  else if (another_condition) {
    // if not condition but another_condition (preferably), do this
  }
  else {
    // if neither of the above, do this
  }
  
  /* arrays */
  // either
  type arr_name[size];
  // or
  type arr_name[optional_size_n] = {item_1, item_2, item_3... item_n}; // fixed n-sized array
  
  return 0; // return 0 to signify successful run of main() function
}
```
***

### 'Compiling' - Behind the 'C'enes
Code needs to be compiled into machine code (virtually unreadable bytecode) before it is able to run
C's language philosophy is that the code can compile anywhere that has a specialised compiler for the hardware and so making the code usable for different things. **:D**
Compilers are made for future users to leverage as tools to have a more convenient time developing (thus supporting the developers).

