# TAD INTERSEÇÃO

## Descrição
Este módulo define o Tipo Abstrato de Dados (TAD) para interseções, pedras e um tabuleiro de Go (Goban). Ele fornece funções para criar, manipular e verificar interseções, pedras e tabuleiros, além de implementar regras do jogo Go.

## Funcionalidades
O módulo inclui as seguintes funcionalidades:
- Criar e verificar interseções no tabuleiro.
- Criar e manipular pedras (brancas, pretas e neutras).
- Criar, modificar e verificar um Goban (tabuleiro de Go).
- Implementar regras como captura de pedras e territórios.
- Cálculo de pontos e verificação de jogadas legais.

## Estruturas Principais

### Interseção
Uma interseção é representada por um tuplo `(coluna, linha)`, onde:
- `coluna` é uma letra de 'A' a 'S'
- `linha` é um inteiro entre 1 e 19

Funções principais:
- `cria_intersecao(col, lin)`: Cria uma interseção.
- `obtem_col(i)`, `obtem_lin(i)`: Obtêm a coluna ou linha de uma interseção.
- `eh_intersecao(arg)`: Verifica se um argumento é uma interseção válida.
- `intersecoes_iguais(i1, i2)`: Compara duas interseções.

### Pedra
Uma pedra é representada por um caractere:
- 'O' para pedra branca.
- 'X' para pedra preta.
- '.' para interseção vazia.

Funções principais:
- `cria_pedra_branca()`, `cria_pedra_preta()`, `cria_pedra_neutra()`: Criam pedras.
- `eh_pedra(arg)`, `eh_pedra_branca(arg)`, `eh_pedra_preta(arg)`: Verificam o tipo de pedra.
- `pedra_para_str(p)`: Converte uma pedra em string.

### Goban
O Goban é representado por uma matriz `n x n` contendo pedras.

Funções principais:
- `cria_goban_vazio(n)`: Cria um tabuleiro vazio.
- `cria_goban(n, ib, ip)`: Cria um tabuleiro com pedras brancas e pretas.
- `coloca_pedra(g, i, p)`, `remove_pedra(g, i)`: Manipulam pedras no tabuleiro.
- `obtem_pedra(g, i)`: Retorna a pedra em uma interseção.
- `eh_goban(arg)`: Verifica se um argumento é um Goban válido.
- `goban_para_str(g)`: Retorna a representação em string do tabuleiro.

### Regras do Jogo
- `jogada(g, i, p)`: Realiza uma jogada no tabuleiro.
- `obtem_cadeia(g, i)`: Retorna a cadeia de pedras conectadas.
- `obtem_territorios(g)`: Obtém territórios livres.
- `calcula_pontos(g)`: Calcula a pontuação dos jogadores.
- `eh_jogada_legal(g, i, p, l)`: Verifica se uma jogada é legal.

## Exemplo de Uso
```python
# Criando um tabuleiro 9x9
board = cria_goban_vazio(9)

# Criando e posicionando pedras
intersecao1 = cria_intersecao('D', 4)
pedra_branca = cria_pedra_branca()
coloca_pedra(board, intersecao1, pedra_branca)

# Exibir tabuleiro
print(goban_para_str(board))
```

## Conclusão
Este módulo fornece uma implementação abrangente do TAD INTERSEÇÃO, PEDRA e GOBAN, permitindo a manipulação de interseções, pedras e tabuleiros de Go, bem como a aplicação das regras do jogo.

