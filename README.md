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
add column cpf dec(11) unique;
describe projeto;
