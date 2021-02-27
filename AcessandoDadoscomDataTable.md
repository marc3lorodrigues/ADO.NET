# Acesso à Dados com DataTable
O acesso ao DataTable pode ser feito através da referencia de coluna e linha

## Exemplo para acesso direto a uma informação do DataTable:
```
DataTable dt;
SqlDataAdapter da;
string texto;
dt = new DataTable();
da= new SqlDataAdapter("SELECT * FROM CLIENTES","SERVER=BICALHO\\SQLEXPRESS2005; uid=sa; pwd=123456");
da.Fill(dt);
texto = dt.Rows[0]["cli_nome"];
```

## Exemplo para acesso através de um DataRow:
```
DataTable dt;
SqlDataAdapter da;
string texto;
dt = new DataTable();
da= new SqlDataAdapter("SELECT * FROM CLIENTES","SERVER=BICALHO\\SQLEXPRESS2005; uid=sa; pwd=123456");
da.Fill(dt);
texto = dt.Rows[0]["cli_nome"];
``` 

## Exemplo para acesso através de um DataRow:
```
DataTable dt;
DataRow dr;
SqlDataAdapter da;
string texto;
dt = new DataTable();
da= new SqlDataAdapter("SELECT * FROM CLIENTES","SERVER=BICALHO\\SQLEXPRESS2005; uid=sa; pwd=123456");
da.Fill(dt);
dr = dt.Rows[0];
texto = dr["cli_nome"];
```
 

 
