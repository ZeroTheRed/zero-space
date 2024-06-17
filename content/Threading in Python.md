I have been learning how to utilize threading for my code and stumbled upon a [Real Python](https://realpython.com/intro-to-python-threading/)on the web while I was searching for a reliable tutorial or a guide to learn that. Threads are essentially components of a process that can be managed independently by the OS's task scheduler. Threads can be executed concurrently using multithreading functions that many OSes provide. If I could figure out how to use threads to control both the yaw and pitch motors simultaneously (think diagonal movement of the spectrometer, rather than doing a manhattan distance-like movement), that would speed things up quite a bit.

It so turned out that I didn't completely understand how threads really work and the complications that may potentiallly arise while using them. Sure, something like
```python
x = threading.Thread(target=lambda: yawmotor.MoveTo(x_pos, 30000))
x.start()
y = threading.Thread(target=lambda: pitchmotor.MoveTo(y_pos, 30000))
y.start()
```
worked but that is acceptable only when I know that this set will be called once alone. Homing the motors is a one-time command. I can get away with the aforementioned setup alright (probably not) but what if I have an objective function to maximize, and that function moves the motors to a specified position, performs an acquisition, and returns the summation of radiation counts? The function will be called several times, and each time the function is called, two threads will be created. The next time the function is called again, two more threads are created, and the second yaw-controlling thread (Thread Y<sub>2</sub>) will attempt to command the yaw motor to move to some position while the first yaw-controlling thread (Thread Y<sub>1</sub>) has already signalled the same motor to move to another position. This naturally creates a conflict (race condition, if you will) that, in my case, caused problems. 

Seems like using a `ThreadPoolExecutor` and setting mutex locks may resolve this issue. I'll have a shot at this soon!

To-do:
- [ ] Read about the following 
	- [ ] Producer-Consumer Threading problem
	- [ ] Threading Objects
- [ ] Implement working multi-threading in my thesis project code


