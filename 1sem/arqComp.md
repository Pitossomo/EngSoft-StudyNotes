# Disciplina: Arquitetura de Computadores

## Tema 1 Base Computacional
### Módulo 1 A Evolução dos computadores
- Máquina de Turing: Precursor matemático do computador
- Gerações dos computadores
  - 1ª Geração: Válvular termiônicas (ENIAC)
  ![image](https://user-images.githubusercontent.com/2355303/224126446-aaef970f-c945-40f8-ae02-e09d7fab3bb2.png)
  - 2ª Geração: Transistores
  - 3ª Geração: Circuitos Integrados
  - 4ª Geração: Microprocessadores
  
---

### Módulo 2 Sistema Computacional
- Hardware: Componentes físicos
  - Processador (CPU)
  - Memória principal (RAM)
  - Placa mãe
  - Periféricos
    - de entrada (mouse, teclado, tela touchscreen, microfone, câmera, placa de rede)
    - de saída (sistema de vídeo, impressora, alto-falante, placa de rede)
  - Memórias secundárias: Disco Rídigo, Discos de Estado Sólido (SSD)
- Software: Programas executados
  - Navegador
  - Jogo
  - Editor de texto
  - Planilha eletrônica
  - Drivers dos componentes físicos
  - Sistema operacional

---

### Módulo 3 Sistema Operacional (OS)
#### Funções do OS
- Camada de abstração entre o hardware e as aplicações do usuário,
para que os demais programas não precisem conhecer sobre o hardware
- Cuidar da alocação do armazenamento e da memória principal
- Cuidar dos processos que correrão em paralelo, simultaneamente, em primeiro plano ou em background
- Determinar quais programas terão acesso ao processador e quando
- Escolher quando os programar passaram o uso do processador para outro programa (escalonador)
    
`Em resumo, o OS gerencia os recursos do hardware e seu acesso pelos demais programas`

#### Histórico
- Anos 70 - UNIX
- Anos 80 - MS-DOS nos computadores pessoais da IBM
- Anos 90 - Consolidação do Windows e Apple
- Século XX - OS para dispositivos móveis

---

### Módulo 4 - Comunicação em Rede
#### Origem da Internet
- Anos 60 - Concepção da ideia de conexão entre computadores espalhados pelos EUA
- Anos 70 - ARPANET montado pelo Departamento de Defesa Norte-Americano
- Anos 80 - Consolidação dos protocolos de conexão e da Internet

#### Conceitos básico
- Endereço IP (Internet Protocol): Sequência de quatro números de 0 a 255
- Roteador: Aparelho responsável por determinar as rotas e transmitir pacotes para que cheguem ao seu destino
- World Wide Web (WWW): Coleção de páginas de hipertexto com links entre si surgida nos início da difusão da internet e acessada pelos navegadores

---
## Tema 2 Componentes de Hardware

### Módulo 1 Estrutura básica de um computador
#### O que é um sistema? Conceitos
- Sistema de computação: Conjunto de partes coordenadas que concorrem para a realização do objetivo de computar dados
- Dados: Fatos em estado bruto a partir dos quais conclusões podem ser tiradas
- Informação: Inteligência e conhecimento derivados dos dados
- Processamento de dados: Atividades ordenadamente realizadas para produzir um arranjo determinado de informações

![image](https://user-images.githubusercontent.com/2355303/224144569-b9864903-1935-4451-8d3b-6212a5cd7134.png)

#### Linguagem de programação
- de baixo nível: usa mnemônicos ao invés de bits, e está relacionada diretamente à arquitetura do computador. P.ex. Assembly e linguagem de montagem
- de alto nível: mais próximos à linguagem humana, maior nível de abstração. P.ex. C++, Pascal, Delphi

#### Organização básica de um sistema de computação
- Composto por dispositivos de entrada, saída, processador, memória principal e memória secundária
![image](https://user-images.githubusercontent.com/2355303/224145543-8837e7f0-3c99-471e-9716-824b343589e8.png)
- Arquitetura de John von Neumann: possibilita à máquina digital armazenar os programas no mesmo espaço de memória que os dados, permitindo a manipulação desses programas
![image](https://user-images.githubusercontent.com/2355303/224145888-58c6c80e-c4f2-4aac-8165-10cb7d01e409.png)

#### Barramentos
- Os sinais elétricos entre os componentes eletrônicos percorrem por fios chamados de barramentos
- Podem de ser de 3 tipos:

| Tipo de barramento | Direção | Origem e destino |
| --- | --- | --- |
| de Dados (BD) | bidirecional | processador e componentes e vice-versa |
| de Endereço (BE) | unidirecionais | do processador para o controlador do barramento |
| de Controle (BC) | --- | sinais específicos de controle e comunicação |

```O total de pinos do processador será igual à soma de BD + BC + BE```

#### Funções básicas de um processador
- As funções executadas pelo processador são simples, como:
  - Executar operações aritméticas
  - Mover um número/dado de um local para outro
  - Mover um número/dado de um dispositivo de entrada ou saída
  - Desviar a sequência de controle
- A operação a ser executada depende do código de operação informado ao processador
- Um conjunto de instruções são todas as possíveis instruções que podem ser interpretadas e executadas por um processador específico
- Um ciclo de instruções é um conjunto de instruções de máquina sequencialmente ordenadas para a execução de um programa

---

### Módulo 2 Subsistemas de processamento, memória e entrada e saída
#### Subsistemas de processamento

Há duas funções principais para o CPU:
- Processamento dos dados
- Controle, composta por:
  - busca da instrução,
  - interpretação das ações, e
  - geração dos sinais para ativação das atividades requeridas (dentro ou fora do processador)

#### Memória 
- A memória é responsável por armazenar e recuperar valores.
- Há diferentes tipos de memórias, usadas conforme o uso requerido seguindo uma hierarquia
![Hierarquia de memórias](https://user-images.githubusercontent.com/2355303/224823454-fe690d26-93e5-4bbc-bbd2-772752ea4790.png)
  - **Registradores**: Estão no topo da hierarquia de memória
    | Tipo de registrador | Descrição        |
    | ------------------- | ---------------- |
    | de Dados | Armazena dados usados pelas unidades de cálculo, separados em número inteiros e ponto flutuante |
    | de Dados de Memória (RDM/MBR) | Transferência externa de dados |
    | de Endereços de Memória (REM/MAR) | Transferência externa de endereços de memória |
    | Contador de instrução/programa (CI/PC) | Busca da próxima instrução |
    | Registrador de instrução (RI/IR) | Armazena instrução |
    | Segmentos | Apontam para determinados segmentos: programa, dados, pilha, etc. |
    | Flags | Indica o resultado de certas instruções |
  - **Cache**: Memória de pequena capacidade entre a memória principal e o processador, para dados usados no momento, transferidos para o CPU em alta velocidade

```
Principio da localidade
  - Espacial: Sempre que o processador realiza um acesso a um endereço, espera-se que o próximo acesso seja no endereço contíguo seguinte
  - Temporal: Espera-se que, quando houver um acesso a um endereço, o próximo seja acessado em um curto espaço de tempo
```

  - **Memória principal**: Memória básica no qual o programa executado e seus dados são armazenados para que o processado busque as instruções
    - Antigamente, usavem método de acesso sequencial, com endereços relativos ao endereço inicial (p.ex. VHS e fitas magnéticas)
    - Posteriormente, passou-se a usar memórias de acesso aleatório (RAM)
    - Memória RAM: usada para escrita ou leitura
    - Organizada em N partes iguais, cada uma com M bits (usualmente M = 1 byte = 8 bits)
    - Cada uma das partes é uma palavra, célula, linha ou setor e é referênciada por um número único chamado endereço.
    - Cada endereço possui a mesma largura E de bits, sendo `2^E >= N`
    - As memórias RAM podem ser:
      - estáticas (SRAM): cada bit com 5 a 7 transistores, sem recarregamento, mais rápidas, requer mais espaço e maior custo, usadas como cache
      - dinâmicas (DRAM): cada bit constituído por um capacitor para o valor do bit e 1 transistor para a leitura/escrita, precisa recarregar capacitor periodicamente (refresh), o que gasta tempo. Usadas como memória principal
    - As memórias DRAM podem ser síncronas ou assíncronas, conforme sua sincronização com o processador
    - O encapsulamento das memórias pode ser:
      - SIMM (Single In Line Memory Module): Contatos elétricos iguals em ambos os lados
      - DIMM (Dual In Line Memory Module): Contatos independentes
  
  - **Memória Secundária**: Usada para armazenamento persistente

#### Subsistemas de entrada e saída


