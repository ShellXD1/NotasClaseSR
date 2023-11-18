# ASCII FTW

# Objetivo
This program has constructed the flag using hex ascii values. Identify the flag text by disassembling the program.You can download the file from [here](https://artifacts.picoctf.net/c/507/asciiftw).
# Solución 
```
Usando ghidra abrimos el archivo y buscamos la funcion principal una vez encontrada damos clicl en el boton verde con un triangulo verde que es de scripting de ghidra el cual nos ahorra muchisimo tiempo.

nos devuelve el siguiente codigo:

from ghidra.program.model.mem import MemoryAccessException

start_addr = currentProgram.getAddressFactory().getAddress("00101184") 
end_addr = currentProgram.getAddressFactory().getAddress("001011fc")

byte_list = [] current_addr = start_addr
	while current_addr <= end_addr: 
		instruction = getInstructionAt(current_addr) 
		if instruction is not None: 
			operand = instruction.getOpObjects(1)[0] # get second operand 
			byte_val = operand.getValue() & 0xFF # convert to unsigned byte 
			byte_list.append(byte_val) 
			
			current_addr = current_addr.next() 
flag = list(map(chr, byte_list)) 
print("Flag:", "".join(flag))


picoCTF{ASCII_IS_EASY_7BCD971D}



```
# Notas Adicionales

# Referencias