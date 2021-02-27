# Manipulando DataReader
Acesso a dados através de um DataReader. Uma vez criado um objeto DataReader é possível acessar os dados do registro através do índice referenciado pela posição/nome da coluna.

#### Acesso pela posição:
```
SqlDataReader dr = cmd.ExecuteDataReader();
string nome = dr[1].ToString();
```
#### Acesso pelo nome da coluna:
```
SqlDataReader dr = cmd.ExecuteDataReader();
string nome = dr["Nome_Cliente"].ToString();
```

 

 

 

 
