Material de orientações para desenvolvimento da missão
prática do 2º nível de conhecimento.

RPG0015  - Vamos manter as informações!

Modelagem e implementação de um banco de dados simples, utilizando como
base o SQL Server.

Objetivos da prática

Identificar os requisitos de um sistema e transformá-los no modelo adequado.
Utilizar ferramentas de modelagem para bases de dados relacionais.
Explorar a sintaxe SQL na criação das estruturas do banco (DDL).
Explorar a sintaxe SQL na consulta e manipulação de dados (DML)
No final do exercício, o aluno terá vivenciado a experiência de modelar a base
de dados para um sistema simples, além de implementá-la, através da sintaxe
SQL, na plataforma do SQL Server.
📍 As práticas devem ser feitas individualmente.

Materiais necessários para a prática

Ferramenta de modelagem DBDesigner, banco de dados SQL Server e
gerenciador SQL Server Management Studio.
Equipamentos:
  - Computador com acesso à Internet.

  - Banco de dados SQL Server, com gerenciador SQL Server Management Studio.

  - Ferramenta de modelagem DBDesigner.

Desenvolvimento da prática

Vamos colocar a mão na massa?! Siga as instruções abaixo para
desenvolvimento desta missão.

👉 1º Procedimento | Criando o Banco de Dados

Baixar e executar a ferramenta de modelagem:
Acessar o endereço https://sourceforge.net/projects/dbdesigner-fork/
Efetuar o download do DBDesigner Fork no formato Zip
Descompactar e executar o aplicativo, como apresentado a seguir:
2.   Definir o modelo de dados para um sistema com as características
apresentadas nos tópicos seguintes:

Deve haver um cadastro de usuários para acesso ao sistema, os quais irão
atuar como operadores para a compra e venda de produtos.
Deve haver um cadastro de pessoas físicas e pessoas jurídicas, com os
dados básicos de identificação, localização e contato, diferenciando-se
apenas pelo uso de CPF ou CNPJ.
Deve haver um cadastro de produtos, contendo identificador, nome,
quantidade e preço de venda.
Os operadores (usuários) poderão efetuar movimentos de compra para um
determinado produto, sempre de uma pessoa jurídica, indicando a
quantidade de produtos e preço unitário.
Os operadores (usuários) poderão efetuar movimentos de venda para um
determinado produto, sempre para uma pessoa física, utilizando o preço de
venda atualmente na base
Observação! No futuro sistema, criado na plataforma Java, será utilizada a
herança na definição de pessoas físicas e jurídicas.

3.   Utilizar o SQL Server Management Studio para criar a base de dados
modelada no tópico anterior:

Logar como usuário sa (System Administrator) e adicionar o logon loja, com
senha loja.
     b.   Logar novamente com o usuário loja, que deve ter permissão para criação
de tabelas e demais estruturas do banco de dados

     c.   Utilizar o editor de SQL para criar as estruturas do modelo.

     d.   Definir uma sequence para geração dos identificadores de pessoa, dado o
relacionamento 1x1 com pessoa física ou jurídica.

     e.   Salvar o script completo para criação do banco de dados em um arquivo
com extensão .sql

✅ Resultados esperados

1. É importante que o código seja organizado.

2. Outro ponto importante é explorar as funcionalidades do DB Designer Fork e
do SQL Server Management Studio para modelagem e criação do banco de
dados.

3. Nesse exercício, é esperado que o estudante demonstre as habilidades
básicas para a modelagem da base de dados em um sistema, além do uso da
sintaxe SQL para a criação das estruturas necessárias.

📝 Relatório discente de acompanhamento

Os Relatórios de Práticas deverão ser confeccionados em arquivo no formato
PDF, com a Logo da Universidade, nome do Campus, nome do Curso, nome da
Disciplina, número da Turma, semestre letivo, nome dos integrantes da Prática.
Além disso, o projeto deve ser armazenado em um repositório no GIT e o
respectivo endereço deve constar na documentação. A documentação do projeto
deve conter:

Título da Prática;
Objetivo da Prática;
Todos os códigos solicitados neste roteiro de aula;
Os resultados da execução dos códigos também devem ser apresentados;
Análise e Conclusão:
Como são implementadas as diferentes cardinalidades, basicamente 1X1,
1XN ou NxN, em um banco de dados relacional?
Que tipo de relacionamento deve ser utilizado para representar o uso de
herança em bancos de dados relacionais?
Como o SQL Server Management Studio permite a melhoria da
produtividade nas tarefas relacionadas ao gerenciamento do banco de
dados?
👉 2º Procedimento | Alimentando a Base

Utilizar o SQL Server Management Studio para alimentar as tabelas com
dados básicos do sistema:
Logar como usuário loja, senha loja.
Utilizar o editor de SQL para incluir dados na tabela de usuários, de forma
a obter um conjunto como o apresentado a seguir:
N2 - 5.png
 (Moderado)
Observação! Usuário op1, com senha op1, e usuário op2, com senha op2, sem
criptografia. Para sistemas reais seria necessário armazenar o hash da senha,
codificado para Base64.

    c.    Inserir alguns produtos na base de dados, obtendo um conjunto como o
que é apresentado a seguir

N2 - 6.png
 (Moderado)
2.   Criar pessoas físicas e jurídicas na base de dados:

Obter o próximo id de pessoa a partir da sequence
Incluir na tabela pessoa os dados comuns
Incluir em pessoa física o CPF, efetuando o relacionamento com pessoa.
N2 - 7.png
 (Moderado)
    d.    Incluir em pessoa jurídica o CNPJ, relacionando com pessoa.

N2 - 8.png
 (Moderado)
3.    Criar algumas movimentações na base de dados, obtendo um conjunto como
o que é apresentado a seguir, onde E representa Entrada e S representa Saída.

N2 - 9.png
 (Moderado)
4.    Efetuar as seguintes consultas sobre os dados inseridos:

Dados completos de pessoas físicas.
Dados completos de pessoas jurídicas.
Movimentações de entrada, com produto, fornecedor, quantidade, preço
unitário e valor total.
Movimentações de saída, com produto, comprador, quantidade, preço
unitário e valor total.
Valor total das entradas agrupadas por produto.
Valor total das saídas agrupadas por produto.
Operadores que não efetuaram movimentações de entrada (compra).
Valor total de entrada, agrupado por operador.
Valor total de saída, agrupado por operador.
Valor médio de venda por produto, utilizando média ponderada.
✅ Resultados esperados

1. É importante que o código seja organizado.

2. Outro ponto importante é explorar a complementação de código nas instruções
SQL a partir do editor do SQL Server Management Studio.

3. Nesse exercício, é esperado que o estudante demonstre habilidade para lidar
com a sintaxe SQL em termos de DML e consultas.

📝 Relatório discente de acompanhamento

Os Relatórios de Práticas deverão ser confeccionados em arquivo no formato
PDF, com a Logo da Universidade, nome do Campus, nome do Curso, nome da
Disciplina, número da Turma, semestre letivo, nome dos integrantes da Prática.
Além disso, o projeto deve ser armazenado em um repositório no GIT e o
respectivo endereço deve constar na documentação. A documentação do projeto
deve conter:

Título da Prática;
Objetivo da Prática;
Todos os códigos solicitados neste roteiro de aula;
Os resultados da execução dos códigos também devem ser apresentados;
Análise e Conclusão:
Quais as diferenças no uso de sequence e identity?
Qual a importância das chaves estrangerias para a consistência do banco?
Quais operadores do SQL pertencem à álgebra relacional e quais são
definidos no cálculo relacional?
Como é feito o agrupamento em consultas, e qual requisito é obrigatório?
