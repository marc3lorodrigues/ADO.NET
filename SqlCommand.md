# SqlCommand
Classe utilizada para executar um comando no banco de dados. O comando poderá ser uma instrução SQL ou a execução de uma Stored Proc.

## Propriedades

#### CommandType     
CommandType.Text = Define a Instrução Sql a ser executada. <br>
CommandType.StoredProcedure = Define uma StoredProc a ser executada. <br>
Commandtype.TableDirect = Define uma tabela a ser manipulada. <br>

#### CommandText             
Define a instrução sql a ser executada.

#### Connection                
Define a conexão a ser utilizada.

#### Parameters	
Armazena uma coleção de parâmetros.

## Eventos

#### Dispose	
Libera recursos do objeto.

#### ExecuteNonQuery
Executa a instrução e retorna o número de registros afetados.

#### ExecuteReader
Executa a instrução e retorna um conjunto de registros do banco.

#### ExecuteScalar
Executa a instrução e retorna a primeira linha/coluna.


## Exemplo de código para criação de um SqlCommand:
```
SqlCommand cmd;
cmd = new SqlCommand();
cmd.CommandType = CommandType.Text;
cmd.Connection = conn;
cmd.CommandText = "INSERT INTO CLIENTE VALUES (1,'Olá Mundo....')";
cmd.ExecuteNonQuery();
cmd.Dispose();
```

## Exemplo de código para criação de um SqlCommand: (Otimizado)
```
SqlCommand cmd = new SqlCommand("INSERT INTO CLIENTE VALUES (1,'Olá Mundo....')", conn);
cmd.ExecuteNonQuery();
cmd.Dispose();
```
 

 

