- `WIN32` is a user-defined flag that may be included in third-party or custom header files. Whereas, ``_WIN32`` is an implementation-reserved namespace already defined by the compiler. It is usually safer to go for the latter. If on Windows 32-bit, ``_WIN32`` will be auto-defined, for example.
- The ``wow64apiset.h`` header file allows you to use the ``IsWow64Process(HANDLE handle, PBOOL boolvar)`` function
- Windows was originally written in C, and at that time, ``bool`` wasn't a defined type per se. Developers had to treat integer literals as boolean variables -- Something like this:
	```c++
	#ifdef TRUE
	#undef TRUE
	#define TRUE 1

	#ifdef FALSE
	#undef FALSE
	#define FALSE 0
```
Today, they don't hold much of a difference as dedicated boolean literals exist now
- `<unistd.h>` is the header file that provides access to the POSIX Standard Library API