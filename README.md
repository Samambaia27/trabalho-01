# trabalho-01
/*criando novo usuario no servidor*/
create user 'lara.rodrigues'@'localhost'identified by'12345';
create user 'izabella.oliveira'@'localhost'identified by'12345';
create user 'luane.gabrielly'@'localhost'identified by'12345';
create user 'tiago.lima'@'localhost'identified by'12345';
create user  'danielgomes'@'localhost'identified by'12345';



/*Aplicando permissã de consulta a todos os arquivos/banco no servidor*/
grant select
on*.*
to danielgomes@localhost;
/*Aplicando permissão de banco inserção em todas as tabelas do banco*/
grant insert
on bd_caso_estudo_vendas.*
to danielgomes@localhost;
/*Aplicativo permissão de banco inserção em todas as tabela definida*/
grant insert 
on bd_caso_estudo_vendas.tb_prod
to tb_func	
grant 
	select(cli_cod,cli_nome,cli_cpf),
    update(cli_end_cep)
on  bd_caso_estudo_vendas.tb_cli
to  danielgomes@localhost;
/**/
grant insert, update, delete 
on `bd_caso_estudo_vendas`.`tb_func`
to danielgomes@localhost;

revoke insert, update
on `bd_caso_estudo_vendas`.`tb_func`
from danielgomes@localhost;

grant delete 
on `bd_caso_estudo_vendas`.`tb_func`
to danielgomes@localhost;

revoke select 
on `bd_caso_estudo_vendas`.`tb_func`
from danielgomes@localhost;

grant insert
on  `bd_caso_estudo_vendas`.`tb_func`
to danielgomes@localhost;
