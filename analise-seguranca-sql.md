Projeto: Investigação de Logs SQL e Tentativas de Acesso

Descrição do Cenário
A equipe de segurança detectou atividades suspeitas no banco de dados da organização. Fui encarregado de investigar a tabela de registros (`log_in_attempts`) 
para identificar tentativas de acesso falhas que pudessem indicar um ataque de força bruta ou acesso indevido fora do horário comercial.

Ferramentas Utilizadas
 **Banco de Dados:** Microsoft SQL Server (T-SQL)
 **Comandos:** `SELECT`, `WHERE`, `AND`, `LIKE`.

 Passo a Passo da Investigação

1. Filtrando Falhas de Login
Para separar acessos legítimos de possíveis ataques, filtrei apenas as tentativas onde o login **não** foi bem-sucedido (flag de sucesso igual a 0).

```sql
SELECT *
FROM log_in_attempts
WHERE success = 0;
