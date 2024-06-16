Configuration settings for nodes
`ros2 param list` - Lists all running params
`ros2 param get <node_name> <param_name>` - Info about param
`ros2 param set <node_name> <param_name> <value>` - Set param value
`ros2 param dump <node_name> > <file_name>` - Saves param values to file. *Default -- standard output*
`ros2 param load <node_name> <file_name>` - Loads param values to node. Read-only files can be modified only at startup
`ros2 run <pkg_name> <exec_name> --ros-args --params <file_name>` - Loads param values at startup
