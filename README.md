CREATE TABLE endereco(
id_endereco serial PRIMARY KEY,
cep char(8) NOT NULL,
rua varchar(100) NOT NULL,
numero varchar(10) DEFAULT 'S/N',
bairro varchar(30) NOT NULL, 
complemento text,
cidade varchar(30)NOT NULL,
estado char(2) NOT NULL
);

CREATE TABLE pessoas(
id_pessoa serial PRIMARY KEY,
nome varchar(100) NOT NULL,
email varchar(100) UNIQUE,
DATA_nascimento date,
altura int CHECK (altura >0),
id_endereco int REFERENCES endereco (id_endereco),
criado_em timestamp DEFAULT now()
);

INSERT INTO endereco(cep, rua, bairro, cidade, estado) 
values('28000000', )
