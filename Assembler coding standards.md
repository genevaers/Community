# Assembler coding standards

## General principles
1. Use simple, easy-to-understand logic
2. Use mostly simple instructions
3. Do not use the location counter in branch instructions (e.g. J *+6)  
4. Use subroutines to break up your code into manageable pieces 
5. Use structured programming concepts and structured programming macros  
   1. Align op-codes and operands in a meaningful way 
6. Use DSECTs to map data areas 
7. Use efficient algorithms and describe in a comment block what you're doing   
8. Request and check feedback from macro instructions 
9. Design internal tables to expand easily 
10. Provide meaningful error messages
11. Use only standard interfaces 
    1. Use macros to get to internals
    2. Don't use constructs that are not defined as a programming interface
    3. Tell the macros your environment (and don't lie) 
       1. The macros change depending on SYSSTATE  
12. Use standard entry/exits whenever possible
    1.  Use the standard linkage conventions defined in the High-Level Assembler User Guide 
    2. Clean up after yourself  
13. Let the Assembler determine lengths (equated symbols, calculated lengths, DSECTs, etc.)  
    1. Remove the use of "magic numbers" 
14. Use meaningful comments 
15. Use meaningful labels 
16. Use meaningful DS instructions 
17. Do not specify BLKSIZE for files
    1. This allows the system to default to the optimal block size  
    2. It also allows you to override the block size in the JCL   
18. Make code reentrant 
    1. Either get your own storage or use an internal stack  mechanism 
    2. Split the code and data areas in your code 
        1.  The hardware benefits from this - there are separate caches for code and data 
19. Designate registers for areas
    1. Then you can avoid saving and restoring them, as the contents don't change 
        1. This is a performance benefit
20. Create internal macros for those repetitive tasks within the product
    1. For example:  error formatting,  internal entry exit
21. Align data to boundaries
    1. At the very least it makes dump reading easier
    2. Also a performance benefit
22. Align the objects of EXecute and EXRL instructions to doubleword boundaries.  
    1. This will prevent us from experiencing minor performance hits when crossing 16-byte boundaries and major performance hits when crossing 256-byte boundaries.  
23. Align the beginning of performance-critical routines on 32-byte boundaries (see http://publibz.boulder.ibm.com/cgi-bin/bookmgr_OS390/BOOKS/IEA2B170/6.2.3?DT=20070605085148)     

## GenevaERS-specific source code format 
1. Start code with a TITLE line 
2. Follow with the standard IBM copyright notice 
3. Follow with the program ID and description 
4. A Change Control Log is in legacy programs and should not be disturbed, but new programs should not include it.  Developers should refer to RTC for the correct information on program modifications.  

## GenevaERS-specific guidelines
1. When a user error occurs, terminate gracefully
   1. Issue the appropriate return code upon completion 
      1. 0 - Successful
      2. 4 - Warning 
      3. 8 - Error 
      4. 12 - Severe Error 
2. Assume that the customer machine supports the instruction set of IBM IBM 3906 (z14, released in July 2017) or later.  
   1. These instructions are described in z/Architecture Principles of Operation, SA22-7832-11 - Twelfth Edition (August, 2017).
   2. You can guarantee that your assembly doesn't use any instructions newer than this level by adding the option OPTABLE(ZS8) to your assembly JCL.  
   3.  Newer instructions can be used, but cannot be the default behavior, and must be paired with a JCL parameter to employ them. 
3.  Assume that the customer machine is running z/OS 2.4 (released July, 2019) or later.  
4.  To avoid confusion with the Branch Register instruction, use the J form rather than the BR form of Branch Relative op codes 
5.  When below-the-bar memory is required, use the STORAGE OBTAIN service rather than the older GETMAIN service. 
6.  When memory is required, use a *conditional* memory allocation, trap any error, report it to the user, and exit gracefully.

