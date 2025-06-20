# BlinkBuzz
I wrote this small but complete library to help with code readability in the SRAD_Avionics code. There were many instances of us having long sections of code that looked like 
```cpp
digitalwrite(PIN, HIGH);
delay(500);
digitalWrite(PIN, LOW);
```
To help make it both neater, shorter, and easier to read, I developed this library, allowing for one line of code that does the same thing:
```cpp
bb.aonoff(PIN, DURATION);
```
The library also has another feature we’d been juggling for some time: letting users know (via beeps) that something had happened, without stopping the code while the beeps play. To this end, I developed an asynchronous feature in the library that allows code to continue execution while a beep is playing. Previously, if you wanted to beep for one second to let a user know an event had transprited, the entire execution of code would stop and wait for that one second beep to play out. Not very helpful for keeping a sensor update loop at >10 Hz. This allows us to send beeps of any length we want to an end user without the code having to wait for it to finish.

I am especially proud of this library because of how neat it is. It has a version that allows you to compile and test it on Windows, it has both async and sync features, it’s incredibly easy to use, and it’s only two files of code. It represents my style, knowledge of C++, efficiency, and documentation skills. It differs from the SRAD_Avionics repo because it is an entire, complete project that is ready for anybody to use. It’s an effective demonstration of how I code.
