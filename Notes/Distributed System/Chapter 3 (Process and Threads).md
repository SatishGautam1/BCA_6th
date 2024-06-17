### Process
- Program on execution, Program on action
- A process is an instance of program running in a computer.
- It consist of an execution environment together with one or more thread (scheduled activities attached to process).
- The following figure shows the layout of process.

| Stack      | -> Temporary data such as method/function parameters return address and local variation                                    |
| ---------- | -------------------------------------------------------------------------------------------------------------------------- |
| **&uarr;** |                                                                                                                            |
| **&darr;** |                                                                                                                            |
| **Heap**   | **-> Dynamically allocated memory to process during its run time.**                                                        |
| **Data**   | **-> Section contain local and global variable.**                                                                          |
| **Text**   | **-> This include the current activity by the value of program counter and the      content of the processor's register.** |

### Process life cycle

![[Pasted image 20240611092727.png]]

- When process execute its passes through various states.
- State name may differ in different OS.
- The OS manage information about a process in process control block.
- Modern OS allow process to divide into multiple thread of execution, which show all process management information.
- This information is held in Thread Context Block (TCB).
- Thread in process can execute different part of program code at a same time.
- They can also execute same part of code at the same time but with different execution state.
- Thread have independent current instruction i.e. they have independent program counter.
- They work with different data i.e. they are working with independent register.

### Process have five states
1. Start/Create
2. Ready
3. Running
4. Waiting
5. Termination

### Thread
- Scheduled activities attached to process
- **Main advantages of having thread are:**
	- Maximize degree of concurrent execution between operation.
	- To enable overlap of computation with input and output.
	- Concurrent processing of client request which reduce server to become bottle neck.

