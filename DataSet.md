# DataSet
Classe utilizada para prover dados desconectados de um banco de dados. Mantém em sua estrutura coleções de objetos que irão representar dados de um banco de dados. A origem de dados pode ser feita através de um adaptador ou um arquivo XML.

## Propriedades

#### DataTable	
Especifica a tabela a ser manipulada
 	 
 

## Exemplo de código para criação de Dataset:
```
SqlConnection conn = new SqlConnection("SERVER=BICALHO\\SQLEXPRESS2005; uid=sa; pwd=123456");
conn.Open();

string SQL = "SELECT * FROM CLIENTES";
SqlDataAdapter da = new SqlDataAdapter(SQL,conn);

DataSet ds = new DataSet();
da.Fill(ds);
```
 

 
