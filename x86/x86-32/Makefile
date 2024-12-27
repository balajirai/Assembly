# Default target
all: help
# .SECONDARY:

# Rule to assemble and link based on the provided file
%.o: %.asm
	nasm -f elf32 -o $@ $<

%: %.o
	ld -m elf_i386 -o $@ $<

# Helper target to display usage
help:
	@echo "Usage: make <filename>"
	@echo "Example: make hello"

# Clean target to remove generated files
clean:
	rm -f *.o