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
This key is unique, it does not allow data to be repeated or repeated, it is the main one, it sort of organizes the dataand avoids confusion (Essa key ela é unica, ela não permite dados repetidos ou ser repedida, ela é a principal, meio queonde organiza os dados e evita bagunça)

### ALTER TABLE users
### MODIFY COLUNM id INT AUTO_INCREMENT, ADD PRIMARY KEY (id);
AUTO_INCREMENT = It keeps the id number for not repead

ADD PRIMARY KEY = Adds a Primary key for colunm and for data

## Foreign Key
This key can have several of them, as it connects the tables, it is as if it took the data from the Primary key and usedit to organize itself, it can also send the data to the Primary key (Essa key pode ter várias dela, pois ela conecta as tableas, é como se ela pegasse o dado da Primary key e usa-se para se organizar, ela pode também enviar os dados para a Primary key)

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

