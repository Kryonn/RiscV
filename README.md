# RiscV

## Instruções
As instruções do RiscV possui uma quantidade fixa de 32 bits, podendo assumir diferentes configurações de acordo com o tipo dela.
#### Tipo R:
As instruções do tipo R são aquelas que realizam operações aritméticas e lógicas, isso inclui: ADD, SUB, SLT, AND, OR, etc. A configuração dos bits desse tipo de instrução segue o seguinte padrão:

![imagem_2024-09-24_083855741](https://github.com/user-attachments/assets/056a3b33-f29c-4d86-8d32-d0d68bbd8417)

* opcode (6-0) - O opcode é o código que define que a instrução será do tipo R, logo todas as instruções do tipo R possui o mesmo opcode.
* rd (11-7) - rd é o registrador de destino do resultado da operação.
* funct3 (14-12) - funct3 é o código que define a operação que será feita(soma, subtração, or, ...).
* rs1 (19-15) - rs1 é o código do registrador que contém o valor do primeiro operando.
* rs2 (20-24) - rs2 é o código do registrador que contém o valor do segundo operando.
* funct7 (31-25) - funct7 é o código que diferencia as operações dentre as do tipo R.




