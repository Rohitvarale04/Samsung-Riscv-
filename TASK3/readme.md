- Decoding RISC-V Instructions: A Visual Guide
----

Instruction Types and Fields

RISC-V instructions are categorized as:


R-type: Register type

I-type: Immediate type

S-type: Store type

B-type: Branch type

U-type: Upper immediate type

J-type: Jump type

Opcode and Function Fields

Opcode: Determines the type of instruction.

func3 and func7: Specify operations within an instruction type.


-----
addi sp, sp, -16

Type: I-Type

Encoding: 0010011 00000 00000 00000 1111111111110000

----


sd ra, 8(sp)

Type: S-Type

Encoding: 0100011 00000 00100 11111 00000 000000001000

----
li a5, 100

Type: I-Type

Encoding: 0010011 00000 00000 00101 0000000001100100

-----

addiw a5, a5, -1

Type: I-Type

Encoding: 1010011 00101 00000 00101 1111111111111111

-----
bnez a5, 10160

Type: B-Type

Encoding: 1100011 00101 00000 00000 0000000000001010

-----

lui a2, 0x1

Type: U-Type

Encoding: 0110111 00010 0000000000000000000000001

-----

addi a2, a2, 954

Type: I-Type

Encoding: 0010011 00010 00000 00010 0000001110111010

----
li a1, 100

Type: I-Type

Encoding: 0010011 00000 00000 00001 0000000001100100

----

lui a0, 0x1c

Type: U-Type

Encoding: 0110111 00000 000000000000000000011100

----

addi a0, a0, 160

Type: I-Type

Encoding: 0010011 00000 00000 00000 0000000010100000

-----

jal ra, 1031c

Type: J-Type

Encoding: 1101111 00000 000000000000000000000000011111001100

-----

li a0, 0

Type: I-Type

Encoding: 0010011 00000 00000 00000 0000000000000000

-----

ld ra, 8(sp)

Type: S-Type

Encoding: 0100011 00000 00100 11111 00000 000000001000

-----

addi sp, sp, 16

Type: I-Type

Encoding: 0010011 00000 00000 00000 0000000000010000


ret

Type: R-Type

Encoding: 1100111 00000 00000 00000 00000 1110011

