### Questão 2(a,b,c)

# Tarefa BD2

## ODBC

ODBC (Open Database Connectivity) é uma interface padrão para acesso a bancos de dados. Ele permite que sistemas de software se conectem a vários SGBDs (Sistemas Gerenciadores de Bancos de Dados) de forma independente da plataforma.

* O pacote pg é o driver oficial recomendado para se conectar ao PostgreSQL a partir do Node.js.
* Seguem os padrões da biblioteca libpq, que é utilizada nas aplicações nativas do PostgreSQL.
* Ao invés de usar ODBC, o pg implementa a conexão de forma nativa, sem a necessidade de drivers ODBC instalados.
* Para gerenciar várias conexões de forma eficiente, o pg utiliza o conceito de pool (pool de conexões).
* Isso é feito através da classe Pool, onde especificamos parâmetros de conexão como BD, usuário, senha etc.
* Ao executar consultas, o driver reutiliza aplicações já abertas do pool, ao invés de criar novas a cada operação.
* Isso melhora o desempenho ao evitar sobrecarga de estabelecer sempre novas conexões.
* Podemos executar consultas/transações através de métodos do pool, como pool.query(), pool.connect() etc.

### Criei os endpoints para a resposta (a, b, c) da questão 5
http://localhost:3000/questao5/a http://localhost:3000/questao5/b http://localhost:3000/questao5/c

## ORM
ORM (Object Relationship Mapping) é uma técnica de mapear objetos de programação para tabelas relacionadas em bancos de dados.

### No Node.js, podemos usar ORMs para:

* Resumo a camada de acesso a dados e consultas SQL.
* Trabalhe com objetos e métodos ao invés de consultas diretas.
* Definir modelos (classes/tabelas) e associações entre eles.
* Realizar operações CRUD de forma simplificada.

### Um dos frameworks ORM mais populares para Node.js é o Sequelize. Alguns pontos:

* Permite definir modelos de nomes de atributos e relacionamentos.
* Conectado a diversos bancos como PostgreSQL, MySQL, Sqlite etc.
* Realiza mapeamento automático de tipos de dados.
* Inclui métodos para criar, ler, atualizar e excluir registros.
* Gerenciar transações de forma agrupada.
* Possui poderosos mecanismos de associação entre modelos.
* Criamos estruturas otimizadas para melhor desempenho.
* Facilita escalabilidade em aplicações com muitos dados.