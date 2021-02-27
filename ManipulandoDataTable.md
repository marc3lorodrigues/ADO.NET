# Manipulação DataTable

## Populando um DataTable:
Uma vez criado um DataAdapter o mesmo poderá popular um DataTable.

#### Exemplo:
    conn.Open();
    DataTable dt = new DataTable();
    SqlDataAdapter da = new SqlDataAdapter("SELECT * FROM PRODUTO",conn);
    da.Fill(dt);

	
## Manipulando as linhas de um DataTable:
Através da propriedade Rows temos acesso as linhas do DataTable/tabela do banco.

#### Exemplo:

```
dt.Rows.Count
```
Retorna o numero de linhas de um DataTable.

```
dt.Rows[i]
```
Recupera a linha informada por i. onde i é o índice da linha.

```
dt.Rows[i][y]
```
Recupera um objeto com a  informação especificada por i e y. onde i é o índice da linha e y é o índice da coluna.

```
dt.Rows[i]"ESP_NOME"]
```
Recupera um objeto com a  informação especificada por i e a coluna. onde i é o índice da linha e "ESP_NOME" é o nome da coluna.

```
dt.Rows.Clear()
```
Elimina as linhas do DataTable.

## Manipulando as colunas de um DataTable:
Através da propriedade Columns temos acesso as colunas do DataTable/tabela do banco.

#### Exemplo:
```
dt.Columns[i]
```
Recupera a coluna informada por i. onde i é o índice da coluna.

```
dt.Columns.Count
```
Recupera a quantidade de colunas do DataTable.

## Percorrendo um DataTable e recuperando as linhas:
Através da estrutura foreach todos as linhas do DataTable é referenciado através do objeto drw.

Exemplo:
```
int codigo;
string nome;
foreach (DataRow drw in dt.Rows)
{
    codigo = Convert.ToInt32(drw["CLI_CODIGO"]);
    nome = Convert.ToString(drw["CLI_NOME"]);
}
```
 

 

 

 

 

 

 

 

 

 

 

 

 

 
