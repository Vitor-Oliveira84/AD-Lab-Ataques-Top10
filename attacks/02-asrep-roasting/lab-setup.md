
# Configuração do Laboratório

1. Criar o Usuário Alvo
Abra o Active Directory Users and Computers (dsa.msc).
Crie um novo usuário (ex: Nome: Admin-Tarefa, Logon: admin_tarefa).
Defina uma senha propositalmente fraca (ex: Verão2026).

2. Desativar a Pré-Autenticação Kerberos
Esta é a configuração que cria a vulnerabilidade:
Clique com o botão direito no usuário criado (admin_tarefa) e selecione Properties (Propriedades).
Vá até a aba Account (Conta).
Na seção inferior, chamada Account options (Opções de conta), role a lista para baixo.
Marque a caixa: "Do not require Kerberos preauthentication" (Não exigir pré-autenticação Kerberos).
Clique em Apply e OK.
