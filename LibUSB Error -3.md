I had recently faced this error while setting up the spectrometer inside the Einstein Cabinet
```
Access Denied, Insufficient Permissions 
```
What could this error be? 
The trace of the error is:
`gccDppConsole.cpp` --> `ConsoleHelper.cpp` --> `DppLibUsb.cpp`
Looking at the DPP LibUSB code, I observed that it was spitting out `-3` as the error code. The same program showed that `-3` translated to an "Access Denied" error. Why was that happening? I tried looking this issue up on the interwebs but in vain :(
Thinking about this, I reasoned that it might be due to connecting the spectrometer to an active USB port (which may possibly be serving a hub). With this train of thought, the error made sense on a higher level. The program would not allow me to establish a complete connection through a self-powered USB cable that is already serving other online devices. However, I am not fully convinced by this explanation. Seems like I have to read more about it.

Reconnecting the spectrometer to a passive USB cable and changing the `deviceID` in the code fixed the issue atleast


To-do:
- [ ] Complete this note by adding relevant code snippets
- [ ] Read more on the error and the internal workings of it