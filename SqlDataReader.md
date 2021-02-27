# SqlDataReader
Classe utilizada para recuperar dados do banco de dados. O DataReader é um objeto que trabalha conectado e devera ser utilizado para recuperar um volume pequeno de dados.
Para acessar os dados de um DataReader deverá ser feito uma referencia as colunas.

## Propriedades
#### HasRows	
Indica se o DataReader possui uma ou mais linhas.
#### IsClosed
Indica se o DataReader está fechado.

## Eventos
#### Read
Avança o ponteiro para o próximo registro.
#### Dispose	
Libera recursos do objeto.
 	 
 	 
 

 

## Exemplo de código para criação e utilização de um SqlDataReader:

```
SqlConnection conn = new SqlConnection("server= BICALHO\SQLEXPRESS2005; database=master; uid=sa ");
conn.Open();
 
SqlCommand cmd = new SqlCommand("SELECT * from cliente", conn);
cmd.CommandType = CommandType.Text;
SqlDataReader dr = cmd.ExecuteReader();
 
while (dr.Read())
    MessageBox.Show(Convert.ToString(dr["CLI_NOME"]));
 ```
