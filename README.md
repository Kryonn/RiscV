# RiscV

## Instruções
As instruções do RiscV possui uma quantidade fixa de 32 bits, podendo assumir diferentes configurações de acordo com o tipo dela.
#### Tipo R:
As instruções do tipo R são aquelas que realizam operações aritméticas e lógicas, isso inclui: ADD, SUB, SLT, AND, OR, etc. A configuração dos bits desse tipo de instrução segue o seguinte padrão:

![imagem_2024-09-24_083855741](https://github.com/user-attachments/assets/056a3b33-f29c-4d86-8d32-d0d68bbd8417) 182

* opcode (6-0) - O opcode é o código que define que a instrução será do tipo R, logo todas as instruções do tipo R possuem o mesmo opcode.
* rd (11-7) - rd é o registrador de destino do resultado da operação.
* funct3 (14-12) - funct3 é o código que define a operação que será feita(soma, subtração, or, ...).
* rs1 (19-15) - rs1 é o código do registrador que contém o valor do primeiro operando.
* rs2 (20-24) - rs2 é o código do registrador que contém o valor do segundo operando.
* funct7 (31-25) - funct7 é o código que diferencia as operações dentre as do tipo R.

##### Exemplos:
funct7  /    rs1    /    rs2    /  funct3   /     rd    /    opcode 

0000000 / 00001 / 00000 /  000  / 00010 / 0110011 - r2 <= r1 + r0

0100000 / 00001 / 00000 /  000  / 00010 / 0110011 - r2 <= r1 + r0

0000000 / 00001 / 00000 /  110  / 00010 / 0110011 - r2 <= r1 | r0

0000000 / 00001 / 00000 /  010  / 00010 / 0110011 - r2 <= r1 < r2

#### Tipo I:
As instruções do tipo I são aquelas que realizam operações com valores imediatos, ou seja, que não estejam em registradores. Nisso, estão incluídos: operações aritméticas com valores imediatos e operações de escrita (load). A configuração dos bits desse tipo de istrução segue o seguinte padrão:

![imagem_2024-09-24_093110451](https://github.com/user-attachments/assets/8650b94f-c824-4677-98c3-1bc045e47946)

* opcode (6-0) - Código de identificação das instruções do tipo I.
* rd (11-7) - rd é o registrador de destino do resultado da operação.
* funct3 (14-12) - funct3 é o código que define a operação que será feita(soma, subtração, or, ...).
* rs1 (19-15) - rs1 é o código do registrador que contém o valor do primeiro operando.
* imm[11:0] (31-20) - imm é o valor do imediato.

##### Exemplos:

 imm[11:0]   /    rs2    /  funct3   /     rd    /    opcode










