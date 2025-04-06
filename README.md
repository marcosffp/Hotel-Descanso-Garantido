# Hotel Descanso Garantido

Bem-vindo ao sistema **Hotel Descanso Garantido**! Este projeto foi desenvolvido para gerenciar as operações de um hotel, incluindo o cadastro e gerenciamento de clientes, funcionários, quartos e estadias. Abaixo, você encontrará uma explicação detalhada sobre o funcionamento do sistema e seus componentes.

---

## Estrutura do Projeto

O projeto está organizado em arquivos que representam diferentes funcionalidades do sistema:

- **`clientes.c` e `clientes.h`**: Gerenciam os dados dos clientes.
- **`funcionarios.c` e `funcionarios.h`**: Gerenciam os dados dos funcionários.
- **`quartos.c` e `quartos.h`**: Gerenciam os dados dos quartos.
- **`estadias.c` e `estadias.h`**: Gerenciam as estadias dos clientes.
- **`main.c`**: Contém o menu principal e integra todas as funcionalidades.

---

## Funcionalidades

### 1. **Clientes**
- **Cadastrar Cliente**: Permite adicionar novos clientes ao sistema.
- **Alterar Cliente**: Atualiza as informações de um cliente existente.
- **Excluir Cliente**: Marca um cliente como excluído (exclusão lógica).
- **Pesquisar Cliente**: Busca clientes por código ou nome.
- **Listar Clientes**: Exibe todos os clientes cadastrados, incluindo pontos de fidelidade.

### 2. **Funcionários**
- **Cadastrar Funcionário**: Adiciona novos funcionários ao sistema.
- **Alterar Funcionário**: Atualiza os dados de um funcionário existente.
- **Excluir Funcionário**: Marca um funcionário como excluído (exclusão lógica).
- **Pesquisar Funcionário**: Busca funcionários por código ou nome.
- **Listar Funcionários**: Exibe todos os funcionários ativos.

### 3. **Quartos**
- **Cadastrar Quarto**: Adiciona novos quartos ao sistema.
- **Alterar Quarto**: Atualiza as informações de um quarto existente.
- **Excluir Quarto**: Marca um quarto como excluído (exclusão lógica).
- **Listar Quartos**: Exibe todos os quartos cadastrados.

### 4. **Estadias**
- **Cadastrar Estadia**: Registra uma nova estadia para um cliente.
- **Baixa de Estadia**: Finaliza uma estadia e calcula o valor total.
- **Pesquisar Estadia**: Busca estadias por código.
- **Listar Estadias**: Exibe todas as estadias registradas.

---

## Como Funciona o Sistema

1. **Inicialização**:
   - Os arquivos de dados (`clientes.dat`, `funcionarios.dat`, `quartos.dat`, `estadias.dat`) são carregados no início do programa.
   - Se os arquivos não existirem, eles serão criados automaticamente.

2. **Menu Principal**:
   - O sistema apresenta um menu com opções para gerenciar clientes, funcionários, quartos e estadias.

3. **Persistência de Dados**:
   - Todas as alterações realizadas no sistema são salvas nos arquivos correspondentes, garantindo que os dados sejam mantidos entre execuções.

4. **Exclusão Lógica**:
   - Clientes, funcionários e quartos não são removidos fisicamente dos arquivos. Em vez disso, são marcados como "excluídos" para preservar o histórico.

---

## Estrutura dos Dados

### Cliente
```c
typedef struct {
    int cod_cliente;
    char nome_cliente[50];
    char endereco[100];
    char telefone_cliente[15];
    int pontos_fidelidade;
    int excluido;
} Cliente;
```

### Funcionário
```c
typedef struct {
    int cod_funcionario;
    char nome_funcionario[50];
    char telefone_funcionario[15];
    char cargo[30];
    float salario;
    int excluido;
} Funcionario;
```

### Quarto
```c
typedef struct {
    int numero;
    int quantidade_hospedes;
    float valor_diaria;
    char status[11];
} Quarto;
```

### Estadia
```c
typedef struct {
    int codigo_estadia;
    char data_entrada[11];
    char data_saida[11];
    int quantidade_diarias;
    int cod_cliente;
    int num_quarto;
} Estadia;
```

---

## Como Executar

- Compile o projeto utilizando o Makefile (se disponível) ou compile manualmente os arquivos `.c`.
- Execute o programa gerado.
- Navegue pelo menu para acessar as funcionalidades.

---

## Observações

- Este projeto foi desenvolvido com foco em aprendizado e prática de manipulação de arquivos em C.
- Para dúvidas ou melhorias, sinta-se à vontade para contribuir!

**Desenvolvido por Gabriela, Luisa e Marcos.**
```
