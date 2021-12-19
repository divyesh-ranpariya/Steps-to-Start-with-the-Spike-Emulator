***************************************************************************************************************************************************
--------------------------------------Basic C and Assembly program Running and Debugging Steps----------------------------------------------------
***************************************************************************************************************************************************
if you are using different folder other than the RISC-V environment variable. So you need to set the environment variable.
   export PATH="$HOME/RISCV/bin:$PATH"
--------------------------------------------------------------------------------------------------------------------------------------------------
Steps to Run the Program:

   1) Wrtie code in editor:
        gedit main.c/S

   2) To generate the object file:
        riscv64-unknown-elf-gcc -o main main.c

   3) Run the executable:
       spike pk main

---------------------------------------------------------------------------------------------------------------------------------------------------

Steps to Debugging Steps:
    After Step 2:
   
   A) Open the generated object/binary file in debug mode: 
         riscv64-unknown-elf-objdump -d main |less

   B) Find the pc value for the main label in the binary i.e 0000000000010146 and note that down.
   
   C) Use below command to enter into interactive debug mode using spike:
         spike -d pk main
   
   D) Following commands can be used for debug operations:
       i) Execute next instruction: run 1 
       ii) Execute next n instruction: run n
       iii) View register content: reg 0 reg_name (i.e. t1,t2 etc)
         
      
 

   