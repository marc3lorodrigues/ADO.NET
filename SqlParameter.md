# SqlParameter
Classe utilizada para representar um parâmetro em um objeto do tipo SqlCommand. O objeto SqlParameters poderá ser criado diretamente no SqlCommand ou criado separado e adicionado no Sqlcommand posteriormente.

## Propriedades	 
#### Direction	
Define a direção do parâmetro. Exemplo direção de entrada.

#### ParameterName	
Define o Nome do parâmetro.

#### SqlDbType	
Define o tipo de dado do parâmetro. O tipo utilizado é o do banco de dados utilizado.

#### Value	
Define o Valor do parâmetro.
 	 
 

## Exemplo de código para utilização de parâmetro. O exemplo abaixo cria o parâmetro separado do SqlCommand.
```
SqlConnection conn = new SqlConnection("server=NOTEBICALHO\\SQLEXPRESS; Database=master; uid=sa; pwd=123456");
conn.Open();

SqlCommand cmd;
cmd = new SqlCommand("INSERT INTO CIDADES VALUES (@NOME)", conn);

SqlParameter param = new SqlParameter();
param.Direction = ParameterDirection.Input;
param.ParameterName = "@NOME";
param.SqlDbType = SqlDbType.VarChar;
param.Value = "Londrina";

cmd.Parameters.Add(param);
cmd.ExecuteNonQuery();
```
 

## Exemplo de código para utilização de parâmetro. O exemplo abaixo cria o parâmetro junto com SqlCommand.
```
SqlConnection conn = new SqlConnection("server=NOTEBICALHO\\SQLEXPRESS; Database=master; uid=sa; pwd=123456");
conn.Open();

SqlCommand cmd;
cmd = new SqlCommand("INSERT INTO CIDADES VALUES (@NOME)", conn);
cmd.Parameters.Add("@nome", SqlDbType.VarChar).Value = "Londrina";
cmd.ExecuteNonQuery();
```
 

## Recuperando o Identificador de AutoIncremento:
```
SqlConnection conn = new SqlConnection("server=NOTEBICALHO\\SQLEXPRESS; Database=master; uid=sa; pwd=123456");
conn.Open();

SqlCommand cmd;
cmd = new SqlCommand("INSERT INTO Teste VALUES (@NOME) SELECT @UltimoID = SCOPE_IDENTITY()", conn);
cmd.Parameters.Add("@NOME", SqlDbType.VarChar).Value = "Londrina";
cmd.Parameters.Add("@ultimoID",SqlDbType.Int).Direction = ParameterDirection.Output;
cmd.ExecuteNonQuery();
MessageBox.Show(cmd.Parameters["@ULTIMOID"].Value.ToString());
``` 

 
