# SQL Notes

## Commands

### CREATE TABLE TableName ( id INT, name VARCHAR (255) NOT NULL COMENT "Name user", email VARCHAR (200) NOT UNIQUE "Email user", addres VARCHAR (100) NOT NULL COMENT "ADDRES user")
VARCHAR = Saying that the data will be of type Stringh and defining how many characters it can have (Falando que o dado vai ser do tipo Stringh e definindo o quanto de caracter ela vai poder ter) 

COMENT = Add your information to the data, if necessary (Adiciona uma informação sua ao dado, caso necessário)

DATE = Says that the data will be of type date (Falando que o dado vai ser do tipo data)

## Value Restrictions
NOT NULL = Makes the data mandatory to fill in (Faz o dado ser obrigatório o preenchimento)

UNIQUE = Makes the data unique, there cannot be two (Faz os dados serem unicos, não pode existir dois)

DEFAULT = It automatically places status on created data (Ele coloca status nos dados criados de forma automatica)

### INSERT INTO nameTable (columnsName, columns2) VALUES ("Name", 1)
Used to insert data into a table (Usado para colocar dados em uma tabela)

### ALTER TABLE nameTable
### MODIFY COLUMN name VARCHAR(200) COMMENT 'Complete name of client'
Way to put a comment in column

### SELECT * FROM nameTable
### WHERE columnsName = "Name" OR "Null"
SELECT = Read the content of the table

WHERE = Fetch data with conditions (Para buscar dados com condições)

"*" = All columns

OR = Operator (How "If, For, +, -, Not " in other languages)

### SELECT * FROM users WHERE name LIKE "%Jeff";
To specifically search for the data you want
(Para buscar especificamente o dado que você quer)

### UPDATE users
### SET id = 4
### WHERE email = "teste@teste.com"
UPDATE = For update the data

SET = Placing the new data that will be updated (Colocando o novo dado que vai ser atualizado)

WHERE = Entering which have certain conditions that will be changed

(Inserindo quais que tem certas condições que serão mudados)


### DELETE FROM users
### WHERE nome = "João"
DELETE = It deletes the data and it never comes back

### DROP TABLE nameTable
That command delete the table

### ALTER TABLE users RENAME login
A command to change table informations

RENAME = It's change the name of table

### MODIFY COLUNM
That command change a information colunm in specific

## Operators

### LIKE
Used to compare patterns (Usado para comparar padrões)

### IN
Belongs to a list of values (Pertence a uma lista de valores)

### BETWEEN
Search within time ranges (Busca dentro de intervalos de tempo)

### AND
Same operator as other programming languages

### OR
Same operator as other programming languages

# Keys

## Primary Key
This key is unique, it does not allow data to be repeated or repeated, it is the main one, it sort of organizes the dataand avoids confusion 
(Essa key ela é unica, ela não permite dados repetidos ou ser repedida, ela é a principal, meio queonde organiza os dados e evita bagunça)

### ALTER TABLE users
### MODIFY COLUMN id INT AUTO_INCREMENT, ADD PRIMARY KEY (id);
AUTO_INCREMENT = It keeps the id number for not repead

ADD PRIMARY KEY = Adds a Primary key for colunm and for data

## Foreign Key
This key can have several of them, as it connects the tables, it is as if it took the data from the Primary key and usedit to organize itself, it can also send the data to the Primary key 
(Essa key pode ter várias dela, pois ela conecta as tableas, é como se ela pegasse o dado da Primary key e usa-se para se organizar, ela pode também enviar os dados para a Primary key)

### ALTER TABLE reservas
### ADD CONSTRAINT fk_reservas_users
### FOREIGN KEY (id_users) REFERENCES users (id);
FOREIGN KEY = Adds a Foreign Key for column and data

ADD CONSTRAINT = For add new rule after table creation

REFERENCES = Means that this column points to other table and colunm

### ALTER TABLE reservas
### ADD CONSTRAINT fk_users
### FOREIGN KEY (id_users) REFERENCES users(id)
### ON DELETE CASCADE; (or ON UPDATE CASCADE)
ON DELETE CASCADE = It delete all data, of father and children

ON UPDATE CASCADE = It update all data, of mom and children

# JOINs (Junções)

## LEFT JOIN
LEFT JOIN = Asking to show all of the left table (the table after the FROM) and those on the right, if there are no results, it will be NULL.
(Pedindo para mostrar todos da tabela esquerda (a tabela depois do FROM) e os da direita se não tiver resultados vai ficar NULL.)

## RIGHT JOIN
RIGHT JOIN = Does the same thing that the LEFT JOIN, but just inverted.

## INNER JOIN

### SELECT * FROM users us
### INNER JOIN table1 t1 ON us.id = t1.id_users
ON = JOIN condition

INNER JOIN = Search for equal values ​​between two tables
(Procurar valores iguais entre as duas tabelas)

# Subquery (Subconsulta)

### SELECT * FROM produtos
### WHERE id NOT IN (SELECT id_users FROM users)
NOT IN = It searches the array of items placed, but it returns the result of the one that is not in the column.
(Faz uma busca em array dos itens colocados, mas ele traz o resultado daquele que não esta na coluna.)

### SELECT users.name, (SELECT COUNT(*) FROM produtos WHERE users_id  = users.id) AS total_produtos FROM users; 
COUNT(*) = Count all users_id within products that are equal to users.id
(Contar todos users_id dentro de produtos que são iguais a users.id)

AS = defining the name of this new lookup column (definindo o nome dessa nova coluna de pesquisa)

# Functions

## Group By
### SELECT COUNT(*), users_id FROM produtos GROUP BY users_id
GROUP BY = It is used to group data from the same 'category'
(É usado para agrupar os dados da mesma 'catecoria')

## Order By
### SELECT COUNT(*) AS Amount_users, users_id FROM produtos GROUP BY users_id ORDER BY Amount_users DESC
DESC = Putting in descending order (Colocando na ordem decrescente)
ORDER BY = To organize the column

# Indices
## Index
### CREATE INDEX idx_nome ON users (nome)
CREATE INDEX = Just read name, but the INDEX is to read less line

### EXPLAIN SELECT * FROM users WHERE nome = "João"
EXPLAIN = shows table performance and more specific information