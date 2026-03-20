
# Configuração do Laboratório

1. Preparação no Active Directory
Abra o Active Directory Users and Computers (dsa.msc).
Vá em View (Exibir) e marque Advanced Features (Recursos Avançados).
Localize o usuário que será o "atacante".

2. Atribuindo as Permissões de Replicação
O segredo do DCSync não está no objeto do usuário, mas sim nas permissões da raiz do domínio.
Clique com o botão direito no nome do seu domínio (ex: lab.local) no topo da árvore à esquerda.
Selecione Properties (Propriedades).
Vá na aba Security (Segurança).
Clique em Advanced (Avançado).
Clique em Add (Adicionar).
Clique em Select a principal e digite o nome do usuário. Dê OK.
No campo Applies to (Aplica-se a), certifique-se de que esteja selecionado This object only (Este objeto apenas).
Na lista de permissões, você deve marcar estas duas permissões específicas:
Replicating Directory Changes (Replicar Alterações de Diretório).
Replicating Directory Changes All (Replicar Todas as Alterações de Diretório).
Clique em OK em todas as janelas.
