# BANCO
/*joga fora um esquema pre existente com o nome Empresa*/
drop database if exists empresa;
/*cria uma nova base de dados com o nome empresa*/
create database empresa;
/*indica qual schema/database sera utilizado*/
use empresa;
/*CRIA UMA TABELA*/
create table cliente(
idCliente int primary key,
nome varchar(100),
sexo Enum('M','F'),
datanasc DATETIME
);
create table Projeto(
idProjeto INT auto_increment,
NOME varchar(45),
HORAS FLOAT CHECK(HORAS>0),
	PRIMARY KEY (idProjeto,nome)
);
/*check */
INSERT into PROJETO
(NOME, HORAS)
VALUES
("FELIPE",1);
/* ALTERA A TABELA DEPOIS ACIONA UMA COLUNA */
alter table cliente
add column primeiro_nome varchar(50);
/*altera o nome da coluna*/
alter table cliente 
change column nome sobre_nome varchar(100);
/*descartar uma coluna*/
alter table cliente
drop cpf;
alter table cliente
change column sexo genero enum('masculino','feminino','outro');

describe projeto;

