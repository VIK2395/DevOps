### 1. About signals
https://www.youtube.com/watch?v=lP7xoqkqDZQ

Processes communicate with each other through signals.

Windows Task Manager alternatives in Linux\
https://www.reddit.com/r/linux4noobs/comments/p2takc/is_there_a_task_manager_equivalent_for_linux/

- `ps`
- `pstree` to find the parent process of a process
- `top`
- `htop`
- `system monitor` out-the-box

### 2. About htop and how to __monitor__, kill processes like in Windows Task Manager. Set task priority
https://www.youtube.com/watch?v=vsEJz9aKGKU

Priority range [-20, 19]. The less this number, the higher priority

There are priority and niceness

### 3. About proc
https://www.youtube.com/watch?v=0XdjODvsRN8

- `proc` intersection between procesess and file system. State of processes in virtual file system(mounted in /proc). The place where the kernel places the information about processes.

### 4. Background vs foreground processes
https://www.youtube.com/watch?v=ghh-8trIFYk&list=PLI-knp71HL3WcQocBNgTc9Cnj9Wg-2Xki&index=3

- A foreground process is a process that interacts directly with the user through the terminal or command line interface. It receives input from the user and displays output to the terminal.
- A background process is a process that runs without user interaction. It does not have control over the terminal, allowing the user to continue using the terminal for other tasks.

Example
- `sleep 30` foreground process
- `sleep 30 &` background process