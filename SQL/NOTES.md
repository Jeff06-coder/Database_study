# SQL Notes

## Commands

### CREATE TABLE TableName ( id INT, name VARCHAR (255) NOT NULL COMENT "Name user", email VARCHAR (200) NOT UNIQUE "Email user", addres VARCHAR (100) NOT NULL COMENT "ADDRES user")




### Value Restrictions
NOT NULL = Makes the data mandatory to fill in (Faz o dado ser obrigatório o preenchimento)

UNIQUE = Makes the data unique, there cannot be two (Faz os dados serem unicos, não pode existir dois)

DEFAULT = It automatically places status on created data (Ele coloca status nos dados criados de forma automatica)

### INSERT INTO nameTable (columnsName, columns2) VALUES ("Name", 1)
Used to insert data into a table (Usado para colocar dados em uma tabela)

### SELECT * FROM nameTable
### WHERE columnsName = "Name" OR "Null"
SELECT = Read the content of the table

WHERE = Fetch data with conditions (Para buscar dados com condições)

"*" = All columns

OR = Operator (How "If, For, +, -, Not " in other languages)

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


## Foreign Key


