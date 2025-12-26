 
🐧 Projeto: Auditoria e Correção de Permissões no Linux

📝 Descrição do Cenário
Como analista de segurança, identifiquei que arquivos confidenciais da equipe de RH estavam com permissões inseguras,permitindo
que qualquer usuário do sistema pudesse lê-los e modificá-los. O objetivo foi auditar as permissões atuais e aplicar o princípio do **Privilégio Mínimo** para restringir o acesso.

🛠️ Ferramentas Utilizadas
 **Sistema Operacional:** Linux (Ubuntu)
 **Comandos Bash:** `ls -la`, `chmod`, `chown`.

 🚀 Passo a Passo da Solução

1. Verificação das Permissões Atuais
Primeiro, verifiquei as permissões do arquivo sensível `folha_pagamento.txt` usando o comando de listagem detalhada.

```bash
ls -la folha_pagamento.txt
