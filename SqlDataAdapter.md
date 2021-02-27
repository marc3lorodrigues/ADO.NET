# SqlDataAdapter
Classe utilizada para adaptar dados de uma fonte de dados em um Dataset.

## Eventos
#### Fill
Preenche um objeto  DataSet ou Datable.

 

 

## Exemplo de código para criação e utilização de um SqlDataAdapter:
```
SqlConnection conn = new SqlConnection("SERVER=BICALHO\\SQLEXPRESS2005; uid=sa; pwd=123456");
conn.Open();

SqlDataAdapter da = new SqlDataAdapter("SELECT * FROM CLIENTES",conn);
DataSet ds = new DataSet();
da.Fill(ds);
 ```
