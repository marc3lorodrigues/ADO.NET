# SQLConection
Classe utilizada para fornecer uma conexão com o banco de dados.

## Propriedades
### ConnectionString
Define/Recupera a string de conexão.

### Database
Retorna o nome do database que está aberto na conexão.

### State
Informa o estado da aplicação.

## Eventos

### Close
Fecha a conexão.

### Dispose	
Libera recursos do objeto.

### Open
Abre a conexão.

## Exemplo de código para criação de uma conexão:

SqlConnection conn;
conn = new SqlConnection();
conn.ConnectionString = "server=TI10\\UNOPAR; Database=master; uid=sa";
conn.Open();

if (conn.State == ConnectionState.Open)
    MessageBox.Show("Conexão Aberta!");
else
    MessageBox.Show("Conexão Fechada!");
conn.Dispose();

 

## Exemplo de código para criação de uma conexão: (Otimizado)

SqlConnection conn = new SqlConnection("server=TI10\\UNOPAR; Database=master; uid=sa");
conn.Open();

if (conn.State == ConnectionState.Open)
    MessageBox.Show("Conexão Aberta!");
else
    MessageBox.Show("Conexão Fechada!");


 
