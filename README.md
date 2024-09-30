# banco
```

```sql
create table funcionarios(
codigo int primary key ,
nome varchar(100),
sobrenome varchar(100),
salario decimal (8,2)
);

alter table funcionarios add dataNascimento date;
```
```sql
create table departamentos(
codigo int primary key,
nome varchar(100)
);


alter table departamentos rename column codigo to id;

alter table departamentos rename column id to IDDepartamento;
```
```sql
create table projetos(
id int primary key,
nomeProjeto varchar(100)
);
``` 
```sql
create table alocacoes(
id int primary key,
IDfuncionario int,
IDProjeto int
);

alter table funcionarios rename column sobrenome to apelido;
```
```sql

create table clientes(
ID int primary key, 
nomeCliente varchar (100) 
);

alter table projetos add IDCliente int;
```
```sql
create table enderecos(
 ID int primary key,
 rua varchar(100),
 cidade varchar(100),
 cep decimal (11) 
 );
 
 alter table funcionarios add IDEndereco varchar(100);
 
 alter table clientes rename column nomeCliente to nomeEmpresa;
```
```sql
create table pedidos(
ID int primary key,
dataPedido date 
);

alter table pedidos add IDcliente varchar(100);
```
```sql
create table itensPedidos(
ID int primary key,
IDPedido int,
IDProduto int
);
```
```sql
create table produtos(
ID int primary key,
nomeProduto varchar(100),
quantidadeProduto varchar(70),
valorProduto decimal(10,2)
);

alter table produtos rename column nomeProduto to descricaoProduto;
```
```sql
create table estoques(
ID int primary key,
quantidade int
);

alter table estoques add IDProduto int;
```
```sql
create table vendas(
ID int primary key,
dataVenda date
);

alter table vendas add IDCiente varchar (100);
```