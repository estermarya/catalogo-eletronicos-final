# catalogo-eletronicos-final

Sistema de catalogo de eletronicos em C, feito para rodar no terminal.
Permite cadastrar produtos, controlar estoque, usar carrinho de compras,
favoritos e gerar relatorio de vendas.

## Como compilar

```bash
gcc -Wall -Wextra -o catalogo *.c
```

## Como executar

```bash
./catalogo        # Linux / macOS
catalogo.exe      # Windows
```

## Funcionalidades

- Cadastro, listagem, busca (codigo, nome, categoria), alteracao e exclusao de produtos
- Controle de estoque (validado no carrinho e descontado na venda)
- Carrinho de compras (adicionar, visualizar, remover, limpar)
- Finalizacao de venda com data e hora
- Favoritos
- Relatorio de vendas na tela e em `relatorio.txt`
- Dados salvos em arquivos `.dat` (com versao e protecao contra arquivo corrompido)

## Estrutura do projeto

| Arquivo | Funcao |
|---|---|
| `catalogo.h` | Constantes e structs; declara as variaveis globais |
| `globais.c` | Define as variaveis globais |
| `entrada.c/.h` | Leitura segura de texto, inteiros e decimais |
| `textos.c/.h` | Comparacao de textos sem diferenciar maiusculas |
| `busca.c/.h` | Busca por codigo (produtos, carrinho, favoritos) |
| `arquivos.c/.h` | Salvar e carregar arquivos .dat |
| `produtos.c/.h` | CRUD e pesquisa de produtos |
| `carrinho.c/.h` | Carrinho e finalizacao de venda |
| `favoritos.c/.h` | Lista de favoritos |
| `relatorio.c/.h` | Relatorio de vendas |
| `main.c` | Menu principal |
