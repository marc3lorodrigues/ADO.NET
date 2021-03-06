# SqlTransaction 
Classe utilizada para fornecer uma transação a conexão.

 

 

## Propriedades
#### Connection
Recupera a conexão associada a transação
#### IsolationLevel
Define a forma de isolamento da transação.
* ReadCommitted (Default) = Os dados inseridos em transações só poderão ser acessíveis apos a confirmação da transação.
* ReadUncommitted = Os dados inseridos em transações poderão ser acessíveis antes da confirmação da transação.


## Eventos
#### Commit
Confirma os dados manipulados pela transação.

#### Rollback
Cancela os dados manipulados pela transação.

#### Save
Salva um ponto de controle de transação.

 	 
 

 

## Exemplo de código para criação e utilização de um Transação Gravando os Dados:
```
SqlConnection conn = new SqlConnection("server=NOTEBICALHO\\SQLEXPRESS; database=master; uid=sa; pwd=123456");
SqlTransaction tran;
tran = conn.BeginTransaction(IsolationLevel.ReadCommitted);

string STRSQL = "INSERT INTO TESTE VALUES (" + textBox1.Text + ",'" + textBox2.Text + "')";
SqlCommand cmd = new SqlCommand(STRSQL, conn, tran);
cmd.ExecuteNonQuery();
tran.Commit();
```

## Exemplo de código para criação e utilização de um Transação Cancelando os Dados:
```
SqlConnection conn = new SqlConnection("server=NOTEBICALHO\\SQLEXPRESS; database=master; uid=sa; pwd=123456");
SqlTransaction tran;
tran = conn.BeginTransaction(IsolationLevel.ReadCommitted);

string STRSQL = "INSERT INTO TESTE VALUES (" + textBox1.Text + ",'" + textBox2.Text + "')";
SqlCommand cmd = new SqlCommand(STRSQL, conn, tran);
cmd.ExecuteNonQuery();
tran.RollBack();

 
