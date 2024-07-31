# SEE retlibc.pdf lab manual for specific objective details for the solutions below


## 3.2 Task 1: Exploiting the vulnerability

After the initial setup, the objective of this project is to get a root shell by exploiting a buffer overflow vulnerability present in the retlib.c program. To achieve this, I modified the exploit.c 
file to include the proper stack addresses to jump to after the buffer overflow is exploited. The proper stack addresses for system() and exit() were discovered by using the Linux GDB debugger on the retlib.c file.
For the address of bin/sh, the MYSHELL system variable needs to set using export MYSHELL=/bin/sh

![retlibc_retlic_c_file](https://github.com/user-attachments/assets/b39217dd-8a50-4162-959f-384b11ae226a)

![retlibc_exploit_c_change](https://github.com/user-attachments/assets/14075b2e-048f-436d-b34f-efc845f02381)

After running the compile_exploit.sh file, our badfile is generated and contains the code to take advantage of the buffer overflow

![retlibc_badfile_created](https://github.com/user-attachments/assets/017908c2-aeb5-4402-8a74-f2377ba12801)

When the buffer is overloaded, my badfile code will make the stack jump to the stack address of system() function, from here the exploit will pass "/bin/sh" to the system function and return a root shell

![retlibc_root_success](https://github.com/user-attachments/assets/fa66616f-310b-465a-9549-0bf3845b27bf)
