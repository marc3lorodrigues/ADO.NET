# Manipulação Dataset

## Populando um DataSet
Uma vez criado um DataAdapter o mesmo poderá popular DataSets com vários DataTables. No exemplo abaixo o DataSet possuirá dois DataTables.

#### Exemplo:
	DataSet ds = new DataSet();

    SqlDataAdapter da = new SqlDataAdapter("SELECT * FROM CLIENTE",conn);
    da.Fill(ds,"Clientes");
    da.Dispose();

    SqlDataAdapter da = new SqlDataAdapter("SELECT * FROM FORNECEDOR",conn);
    da.Fill(ds,"Fornecedores");
    da.Dispose();

## Acessando um DataTable:
Uma vez criado um objeto DataSet poderá ser acessado os DataTable do mesmo através do índice ou do nome da Tabela.

#### Exemplo:
        Acesso pela posição.
        DataTable dt = ds.Tables[0]; 

        Acesso pelo nome.
         DataTable dt = ds.Tables["Professores"]; 

		
## Contando os DataTables de um DataSet:
Considerando que a propriedade Tables do DataSet é uma coleção de DataTables a mesma possui uma propriedade Count.

 

#### Exemplo:
```
DataSet ds = new DataSet();
ds.Tables.Count;
```
 

 
