# Real-Time-operating-system-topic-
 # C program to illustrate use of fork() &amp; exec() system call for process creation any many more
# want  to  buy me a coffee ☕🍵❤️ 8867303660@paytm
# The necessary header files are included.
1.The main() function begins.
2.A variable pid of type pid_t is declared to store the process ID returned by fork().
3.ret is set to 1, but it is not used in the program.
status is used to store the status of the child process after it has finished executing.
4.The fork() system call is invoked, creating a child process. The return value of fork() is stored in pid.
5.If pid is -1, it means an error occurred during fork(), and an appropriate message is printed. The program exits with a failure status.
6.If pid is 0, it means the code is running in the child process. The child process prints its own process ID (getpid()) and the process ID of its parent (getppid()).
7.An array argv_list[] is created, which holds the command-line arguments for the ls command: ls -lart /home.
8.The execv() system call is used to replace the child process with the ls command. The first argument is the filename associated with the file being executed (ls), and the second argument is the array of command-line arguments. If execv() succeeds, the child process terminates, and the ls command is executed.
9.If execv() fails, the child process exits with a status of 0.
10.If pid is not 0, it means the code is running in the parent process. The parent process prints its own process ID and the process ID of its parent's parent (getppid()).
11.The parent process calls waitpid() to wait for the child


When the code is executed, it first creates a child process using fork(). The child process then prints its own process ID and the process ID of its parent using getpid() and getppid() respectively. It then uses execv() to execute the "ls" command with the provided arguments.
In the parent process, it prints its own process ID and the process ID of its parent's parent. It also uses waitpid() to wait for the child process to complete execution. Afterward, it checks the status of the child process and prints appropriate messages based on the outcome.
Overall, the code seems to be correctly structured and demonstrates the usage of fork() and exec() system calls.
To run the gcc command in Ubuntu, you need to have the GCC (GNU Compiler Collection) installed on your system. If you haven't installed it yet, you can do so by running the following command in the terminal:
# Copy code
sudo apt install Gcc

Once GCC is installed, you can use the gcc command to compile C programs. Here's an example command to compile a C program named "program.c" and generate an executable file named "program":
# Copy code
gcc program.c -o program

gcc is the command to invoke the GCC compiler.
program.c is the name of the C source file you want to compile.
-o program specifies the output file name for the compiled program.

After running the gcc command, if there are no errors in your C program, it will generate an executable file named "program" in the current directory. You can then run the compiled program using the following command:

# Copy code
./program





