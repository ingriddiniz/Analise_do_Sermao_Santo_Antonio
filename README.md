# Analise do Texto "Sermão de Santo António aos Peixes"
Análise de texto usando Python <br>
<br>
Este é um projeto da cadeira de Programação 2 proposto pela Faculdade de Ciências da Universidade do Porto, cujo objetivo é análisar textos a partir de ficheiros de texto.
<br>
Neste projeto processou-se o texto completo do *Sermão de Santo António aos Peixes* do *Padre António Vieira*,no qual foram extraídas métricas simplese feita uma reformatação do texto.
  
## Tarefa 1

Foi feito um download do ficheiro [sermao.txt](sermao.txt), que contém o texto integral do *Sermão de Santo António aos Peixes* do *Padre António Vieira*.

Aprimeira função `leTexto` lê o conteúdo de um ficheiro de texto para uma lista de linhas de texto, em que cada linha de texto é uma string sem caracteres newline.

## Tarefa 2

A função ``organizaSermao`` organiza uma lista de linhas de texto num tuplo (título,introdução,lista de capítulos), em que cada capítulo é um tuplo (número,lista de parágrafos). Cada linha do título, introdução e parágrafo é por sua vez uma lista de palavras (com pontuação).
Por exemplo, para um sermão dado como a lista de linhas:
```python
['SERMÃO DE EXEMPLO'
,''
,'A título de exemplo.'
,'Veni, vidi, vici.'
,''
,'I'
,''
,'Parágrafo um.'
,'Parágrafo dois.'
]
```
O resultado seria:
```python
(['SERMÃO','DE','EXEMPLO'],[['A','título','de','exemplo.'],['Veni,','vidi,','vici.']],[('I',[['Parágrafo','um.'],['Parágrafo','dois.']])])
```

Algumas funções auxiliares foram criadas para auxiliar nessa tarefa:
- A função `separaLinha` que parte uma linha (string sem newlines) numa lista de palavras;
- A função `separaLinhas`, que parte uma lista de linhas numa lista de listas de linhas, usando como delimitador strings vazias;
- A função `organizaCapitulos`, que recebe uma lista de listas de linhas correspondente ao texto (sem linhas em branco) dos capítulos de um sermão e retorna uma lista de capítulos como descrito em cima.


## Tarefa 3

As funções seguintes recebem como argumento um sermão organizado, como o descrito na Tarefa 2:

- A função `totais` retorna um tuplo com os números totais de capítulos, parágrafos e palavras (todas as palavras do texto, incluindo título, descrição e capítulos);
- A função `deusPeixes` retorna quantas vezes as palavras 'Deus' e 'peixes' ocorrem no mesmo parágrafo;
- A função `maiorParagrafo` retorna o nome do capítulo com maior média de palavras por parágrafo. Caso haja mais do que um capítulo com a maior média, deverá retornar a primeira ocorrência. Assumiu-se que a média de um capítulo sem parágrafos é 0.

## Conclusão
O projeto permitiu aplicar conceitos práticos de processamento de texto e manipulação de dados em Python. Através das funções implementadas, conseguimos obter insights sobre o sermão e extrair informações relevantes para análise. Essa abordagem demonstrou a utilidade da programação para explorar e compreender textos de forma mais eficiente.
