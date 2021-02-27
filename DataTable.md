# DataTable
Classe utilizada para representar uma tabela do banco de dados. É composta de coleções de objetos como DataColumn e DataRow que correspondem a estrutura de uma tabela de um banco de dados relacional.

## Propriedades	
#### Columns	
Armazena a coleção de colunas da tabela.
#### Rows	
Armazena a coleção de linhas da tabela.
#### TableName	
Define o Nome da tabela.
 
 
#### Exemplo de código para criação de DataTable:
```
SqlConnection conn = new SqlConnection("SERVER=BICALHO\\SQLEXPRESS2005; uid=sa; pwd=123456");
conn.Open();

string SQL = "SELECT * FROM CLIENTES";
SqlDataAdapter da = new SqlDataAdapter(SQL,conn);

DataSet ds = new DataSet();
da.Fill(ds);

DataTable dt = new DataTable();
dt = ds.Tables[0];
 ```

 
