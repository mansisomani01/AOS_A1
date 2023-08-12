# AOS_ASSIGNMENT1

### ASSIGNMENT1_1:- 
### OVERVIEW
1. I have tested this code using relative path.
2. In this question we need to reverse the contents of the file and store the result in a new file in the directory named “Assignment1_1”.

### EXPLANATION OF THE CODE:- 
1. Here , main function takes command line arguments. It assigns index-1 to input_file_name . If number of arguments is not 2 then it prints an error message.
2. After that, I created a directory named Assignment1_1 using mkdir function. If status is equals to 0 then it indicates success .
3. Input_fd opens a file specified by input_file_name for reading using the open function. If input_fd = -1 then there is error in opening the input file.
4. After that fstat function is used to retrieve the information about the file associated with the file descriptor input_fd.
5. Then mmap function is used to map the contents of the file associated with input_fd into memory. It assigns the starting memory address of the mapped data to the pointer address_Input. The PROT_READ flag indicates that the memory should be mapped for reading. 
6. ftruncate function is used to set the size of the output file associated with output_fd to the same size as the input file
7. Now agaim mmap function is used to map a region of memory for writing in the output file associated with output_fd. It assigns the starting memory address of the mapped area to the pointer address_Output. The PROT_WRITE flag indicates that the memory should be mapped for writing. 
8. Now I'm using for loop which iterates through memory mapped input file and reverses its content by copying it into memory mapped outpiut file.
9. After that progress of reversal is displayed in percentage that how much file is reversed.
10. cout.flush() is used to ensure that output is immediately displayed without buffering.
11. At last munmap function is used to unmap the memory regions previously mapped for input and output files and then it closes both input and output file descriptors using close.

```
$ g++ 2023201028_A1_Q1.cpp
$ ./a.out <input file name>
```

### ASSIGNMENT1_2:-
### OVERVIEW
1. I have tested this code using relative path.
2. In this question we need to reverse a specific portion of the file and store the result in a new file in the directory named “Assignment1_2”.

### EXPLANATION OF THE CODE:-
1. Here, main function takes command-line arguments and expects 3 command-line arguments an input file name, a start character, and a stop character.
2. If number of arguments is not equals to 4 then it will throw an error message .
3. After that, I created a directory named Assignment1_2 using mkdir function. If status is equals to 0 then it indicates success.
4. Input_fd opens a file specified by input_file_name for reading using the open function. If input_fd = -1 then there is error in opening the input file.
4. After that fstat function is used to retrieve the information about the file associated with the file descriptor input_fd.
5. Then mmap function is used to map the contents of the file associated with input_fd into memory. It assigns the starting memory address of the mapped data to the pointer address_Input. The PROT_READ flag indicates that the memory should be mapped for reading.
6. ftruncate function is used to set the size of the output file associated with output_fd to the same size as the input file
7. Now agaim mmap function is used to map a region of memory for writing in the output file associated with output_fd. It assigns the starting memory address of the mapped area to the pointer address_Output. The PROT_WRITE flag indicates that the memory should be mapped for writing.
8. Logic is same as 1st question but here we have two pointers start and stop in between that we don't have to reverse else do reversing of 1st character to start_char-1 and then stop_char+1 to end.
9. So, for that we will create 3 for loops and implementing the above logic.
10. After that progress of reversal is displayed in percentage that how much file is reversed.
10. cout.flush() is used to ensure that output is immediately displayed without buffering.
11. At last munmap function is used to unmap the memory regions previously mapped for input and output files and then it closes both input and output file descriptors using close.

```
$ g++ 2023201028_A1_Q2.cpp
$ ./a.out <input file name> <start_index> <end_index>
```

### ASSIGNMENT1_3:-
### OVERVIEW
1. I have tested this code using relative path.
2. In this question we need to check the permissions for the two files and the directory and check whether the content in the new file are the reverse of the old file.

### EXPALNATION OF THE CODE:-
1.
