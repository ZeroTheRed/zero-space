https://roboticsbackend.com/ros2-package-for-both-python-and-cpp-nodes/

`colcon build --symlink-install` 
Build process fails because of spiked CPU usage and memory exhaustion. Culprit line: `c++: fatal error: Killed signal terminated program cc1plus`
To fix this issue, reduce the number of parallel threads in the compiler process. Follow this -> https://answers.ros.org/question/368106/c-fatal-moveit-2-error-killed-signal-terminated-program-cc1plus-compilation/