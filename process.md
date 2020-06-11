### Q1 what is process   
A process is  program in execution. This means, for example, that if you open up two browser windows then you have two processes, even though they are running the same program.     
The life-cycle of a process can be described by a state diagram which has states representing the execution status of the process at various times and transitions that represent changes in execution status.     
The operating system maintains management information about a process in a process control block (PCB).     
Modern operating systems allow a process to be divided into multiple threads of execution, which share all process management information except for information directly related to execution. This information is held in a thread control block (TCB).     
![StateDiagram](https://3.bp.blogspot.com/-n_vl4GFz4Dk/VGYzByWKXmI/AAAAAAAAAYg/uUiKyUtSETQ/s1600/process.png)       
   
New:-  If the process is in new state that means either the process is under creation or is being created.                 
Ready:- After the successful creation of a processit is placed in Ready state by Long Term Scheduler. In this state process will wait to be assigned to a processor.In this state we can have a multiple no. of processes.     
Running:- From the Ready state one of the process is selected and it will be scheduled or Dispatched to the Running State by Short Term Scheduler. If a process is in Running state that means instructions of the process are being executed.Only one process will reside in memory at any point of time.             
Waiting:- If any running process require any input/output operation the process will be moved into wait state.     
Terminated:- The Process has finished execution.            
Suspended Ready:- A process moves from ready state to suspended ready due to more priority for other processes.     
Suspended blocked:-  A process moves from waiting state to suspended blocked state due to process might be consuming more memory.     
* Note that ready state, running state and waiting state are always resides in main memory and new state, suspended ready and suspended blocked state resides in secondary memory.     
There are four types of process model:    
(i) Two state process model:![](https://lh4.googleusercontent.com/JKSVHO8RlAkl-ovS5L2Eltuc696DQod2xisEbEJwmQwJPa2gvK4H3h7Xw3KJlz1NOvsq1ElorrU0zwkGCjB0ERt-E1mv7POWOcVrObNODYq29FdbsxA3cWi7v5yIOi7Cg7Yu5pzj)    
(ii) Five state process model: ![](https://lh4.googleusercontent.com/DL_rdOo_0W9bcyQbJsCzLnWBatUwfx82vsyTTH-Q5Hcj-fz4o9e5Ot8EoAlWUqCW_I-oTRTPOczbIrQcvHbZ5v1M3XmIK04-Y4oX_dR56SnZERQKwCBV5JFtrKTcYIVRf-gtATdI)   
(iii) Six state process model:![](https://lh3.googleusercontent.com/tj1rH8c96JmVOnXOnvGPhG3sM_ZoLQ8qSoUp0fbDCf965MZno8Le7RKKlI3rsKvLd9ipWjWJPffguuDO_5Eyd1KoERDKBSGAskhTRyEGHxJ9F1-Jq02FzLdc_n7D3VLOa2MFGNDi)      
(iv) Seven state process model:![](https://lh3.googleusercontent.com/op9wkPQxMQoNrqS6RPeoMrBqoit7PsIp4IhO5ZnvncLV5W9_5ATibB0jno_FtsHh2f6kfsntXZJcYEqDL9ssiBDwu9Z7VpzOTjLbV6Chd8fAJbYm3x7hBxpAmrlo6_rb48hPEGes)      

Where R = Running, W = Waiting, T = Terminated, SB = Suspended block, and SR = Suspended ready state    

#### Process Transitions:     

Transition from new state to ready state occurs when a process is created.    

Transition from ready state to running state occurs when CPU decides(using process scheduling algorithm) which process will run next.    

Transition from running state to ready state occurs when process preempted(acquire in advance).    

Transition from running state to waiting state occurs when process required I/O event.       

Transition from waiting state to ready state occurs when I/O event has completed.                

Transition from running state to terminated state occurs if process has finished its execution.                   

#### Types of Process: There is three type of process:

CPU - Bound: Process needs more service by CPU than I/O service.        

I/O - Bound: Process needs more I/O service than CPU service.             

Interactive: Process spends more time in waiting queue than CPU burst time.              


   
![](https://lh5.googleusercontent.com/TWGiCxVYJibvCT-WCIcpnRU62V5LOzVupixCiEWe5bkfezJpKlBK6H6esqJNUZz29NAOGHPuEt9hjhrlrwsimggiKOdbAQOVGP_bRdT_eoTvt83-bCJ4ECHq7Hjx_0iAzPQrnZpp)       
* There is two types of processes:     
(i) System process: These process can not be preempted and executed in privileged mode.     

(ii) User process: These process can be preempted and executed in user mode.     

Every process has three parts first is executable program or code section, second is data section and third is context section. Context section of a process contains stack and process control information which managed by operating system. Code and data section of a program are called as user address space.      
![](https://lh5.googleusercontent.com/B_HHIoKbXmMIX5yRL3f8W7U6GsYezB1EbR5cXkp94OE7Wk_cElFqaDN3h4pZpr6g1BwNQarXP1ydP9NYNuhwAzAsGqH-iL73JJ4S7-mHI9P7X7FAIx1TAXAsvzsUzTTzD9GTl9rh)      

Process Control Block(PCB): Each process has its own process(or task) control block(PCB).    
We can differentiate processes using process id. Process state defines current state of process; process state can be new, ready, running, waiting etc. Program counter contains address of next instruction to be executed. I/O status information includes list of allocated open devices, list of allocated open files etc. Generally, every PCB has three grouped informations:     

Process identification data contains has numeric identifier, parent identifier, user identifier etc.             

Process control information contains process state information, links to other process memory privileges, scheduling etc.             

CPU state information contains stack pointers, user visible registers, control and status registers etc.              
![](https://lh3.googleusercontent.com/zITpxKul3MRg09ZNZZQDV2ySazrsZdlA9B94nvV283cDpduShF1RJRselr8QZ4TVWvcgtNEC5ZS1uWYfNaufi998CO_Uy-3O0-BERsQ1SL1UZRghS50VvIbd6zT6_OAEuqoKOwgt)    

#### What is PCB (Process Control Block)
PCB is a data structure in the OS and it contains all the information about a process. The following information is stored in PCB;    
* 1.Process ID    

When the OS converts a program into the process then OS assigns process ID to each process. This Process id becomes the unique identification of that process and it also helps in distinguishing that process from all other processes existing in the system.The operating system will allocate the value 0 to the first process that arrives in the system, number 1 to the next process and continues till n-1.     
  
* 2.State of the process   

PCB maintains the record of the state of each process. A process can be in new, waiting, ready, running and can be in the terminated state.

  
* 3.Program counter    

Program counter is used to point to the address of the next instruction to be executed in any process. This is also managed by the process control block.    

* 4. Process Priority   
The priority of the process is a numeric value, lesser the value, greater is the priority of that process. The priority of the process can be assigned externally by the user or by the operating system itself.     

* 5. Process Privileges   

PCB maintains the record of all the privileges assigned to each process. For example privileges of reading, Write, Copy, etc.  

* 6.  Register Information (hold temporary values)   
Whenever an interrupt occurs and there is a context switch between the processes, the temporary information is stored in the registers. So, that when the process resumes the execution it correctly gains from where it leaves. CPU registers are used to hold those temporary values or information.   

* 7.Memory management information   

PCB maintains the record that how much memory is available for use and how much memory is allocated to the processes etc.   

* 8.I/O status information    

Interprocess communication information.Sometimes a process works independently and sometimes some processes work together to achieve a big task.    

* 9.Accounting information   

OS can count the different parameters like hard disk, CPU and RAM usage etc.       

* 10. PCB Pointer   
TO maintains the hierarchy of all the processes so that a parent process could locate all the child processes it creates easily.      

* 11 .List of Open Files    
 It contains the information of all the files that is required by the program during its execution.This information is also useful for the operating system. Because it helps the operating system to close the all opened files which are not closed explicitly at the termination of the program.   

#### Q.2 Inter Process Communication    
Inter Process Communication is a mechanism which allows processes to communicate with each other and synchronize their actions. Whatever process is present in the system, they can communicate with each other. It is a method of cooperation.       

* There are two types of processes –

Independent Process: An Independent process is not affected by other executing processes.             
Cooperating Process: A Cooperating process can be affected by other executing processeses.                  


#### Why do we use inter process communication 

1. Information Sharing: Multiple processes can share same information to perform some tasks. In such scenarios, inter process communication helps. There may be a scenario when a process needs to access remote process. In such case, this method of communication helps.            
2. Resource Sharing: We can do with the help of inter process communication.            
3. Communication speed: Computational speed will also increase if inter process communication method is used to communicate between processes.          
4. Modularity: An architecture is break down into different cooperating modules to increase the efficiency. All the modules cooperate using inter process communication method.            

* Processes can communicate with each other by using two ways –           

1. Shared Memory             
2. Message Passing              

##### 1. Shared Memory    
Shared memory is an efficient way to share data between processes. One process will create a memory portion which other processes can access if allowed.      
![](https://i2.wp.com/tutorialwing.com/wp-content/uploads/2018/09/tutorialwing-os-shared-memory-example.png?w=743&ssl=1)     
`Image (a)`    
Process A generate information about certain resources and keeps records in shared memory. When process B needs to use that information, it will check the record stored in shared memory and take note of the information generated by process A and act accordingly. Thus, processes can use shared memory for extracting information as a record from other process as well as for delivering any specific information to other process.    
`Image (b)`      
Whenever process A uses some shared memory, it sends information to the kernel (operating system). When process B wants to perform some operation, it first checks the Kernel if any other device is using that resources or not. If any process is using that resource, it will take other resources which is free.     
   
##### 2. Message Passing       
In message passing, there is no use of shared memory. If two processes A and B want to communicate with each other, at first, they establish a communication link. After this, they can start exchanging messages using basic primitives.       
They need atleast 2 basic primitives–     
* (a) Send (message, destination) or Send(message)    
* (b) Receive (message, host) or Receive(message)    

A standard message has two parts –     
(a) Header    
(b) Body     

Header contains message type, source id, destination id, message length and control information. Control information contains sequence number, priority, action to do if runs out of space etc.     
Body contains the actual message.     
Generally, any message is sent using FIFO style.      

Mode of communication between two processes can take place in two ways:    

Direct Addressing    
Indirect Addressing    
* 1. Direct Addressing of Message Passing   
In this type, the two processes need to know the name of each other to communicate. This become easy if they have the same parent.    

Example:    
If process A send message to process B, then, basic primitives will be –   

Send (B, message);    
Receive (A, message);     
At first, Processes A and B establish a communication links. Then, they start sending messages. In this example, process A is sending message to process B.    
Process only need to know each other’s identity. In this type, link is associated with exactly two processes. Usually link is bidirectional but it can be unidirectional. Here, receiver knows the identity of sender. This type of direct communication is known as `symmetric addressing`.      
![symmetric addressing](https://i1.wp.com/tutorialwing.com/wp-content/uploads/2018/09/tutorialwing-os-direct-addressing-example.png?w=449&ssl=1)   
Asymmetric addressing: In this type, only sender will name receiver for sending the message. There is no need for receiver to name the sender for receiving the message. This addressing is also known as `asynchronous addressing`.     
![asynchronous addressing](https://i0.wp.com/tutorialwing.com/wp-content/uploads/2018/09/tutorialwing-os-asymmetric-addressing.png?w=510&ssl=1)     

##### 2. Indirect Addressing of Message Passing
In this addressing, message is sent and received using a mailbox. A mailbox can be abstractly viewed as an object into which message may be placed. Message may be extracted by a process.    

In this type, sender and receiver processes should share a mailbox to communicate.    

Tutoriawing operating system Indirect Addressing Example of inter process communication Indirect Addressing Example   

Below are the types of communication link made through mailbox:    
  
One to one link: One sender wants to communicate with one receiver. So, only one link will be established.    
Many to one link: Multiple senders want to communicate with single receiver. Example: In client-server system, there are one server process and many client processes. Here, mailbox is known as a port.    
One to Many link: One sender wants to communicate with multiple receivers. That is broadcasting a message.            
Many to Many link: Multiple senders want to communicate with multiple receivers.         
![Indirect Addressing](https://i2.wp.com/tutorialwing.com/wp-content/uploads/2018/09/tutorialwing-os-indirect-addressing-example.png?w=624&ssl=1)     
 
###### Examples of Inter Process Communication
Some examples of Inter process communication are –   
 
Posix: It uses shared memory method.  
Windows XP: It uses message passing method.   
Mach: It uses message passing method.  
Pipes:Pipes − Communication between two related processes. The mechanism is half duplex meaning the first process communicates with the second process. To achieve a full duplex i.e., for the second process to communicate with the first process another pipe is required.    
Server: 

#### Q.3 Thread  
A thread is a simple path of execution within a process. A big work is divided into parts and each of them is assigned to a unit of execution called a thread. Threads share data structures that are modified by another thread at a time and also because threads shares the same address space.     

##### Process vs Thread
• Processes are difficult to create because it needs a duplication of the parent process and memory allocation whereas threads are easy to create since they do not require a separate address space.    

• Threads are used for simple tasks while processes are used for heavy-weight tasks such as execution of an application.   

• Processes do not share the same address space, but threads within the same process share the same address space.   

• Processes are independent of each other, but threads are inter-dependent as they share the same address space.   

• A process can consist of multiple threads.    

• Since threads share same address space, virtualized memory is only associated with processes but not with threads.    
• Each process has its own code and data whereas the threads of processes share same code and data.   
• Context switching between processes is much slower than the context switching between threads of the same process.   
• Processes have overheads but not threads.     



 





    

