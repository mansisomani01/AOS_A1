# AOS_ASSIGNMENT1

# ASSIGNMENT1_1:- 
I have tested using relative path that is I have tested in same directory itself.
In this question we need to reverse the contents of the file and store the result in a new file
in the directory named “Assignment1_1”.

# Explanation of code:- 
1. Here , main function takes command line arguments. It assigns index-1 to input_file_name . If number of arguments is not 2 then it prints an error message.
2. After that, I created a directory named Assignment1_1 using mkdir function. If status is equals to 0 then it indicates success .
3. Input_fd opens a file specified by input_file_name for reading using the open function. If input_fd = -1 then there is error in opening the input file.
4. After that fstat function is used to retrieve the information about the file associated with the file descriptor input_fd.
5. Then mmap function is used to map the contents of the file associated with input_fd into memory. It assigns the starting memory address of the mapped data to the pointer address_Input. The PROT_READ flag indicates that the memory should be mapped for reading. 
ftruncate function is used to set the size of the output file associated with output_fd to the same size as the input file
mmap function to map a region of memory for writing in the output file associated with output_fd. It assigns the starting memory address of the mapped area to the pointer address_Output. The PROT_WRITE flag indicates that the memory should be mapped for writing. I
