
# Configuração do Laboratório

1. Abrir o Console de Gerenciamento
No seu Domain Controller (ou máquina com RSAT instalada), pressione Win + R, digite gpmc.msc e dê Enter.

Navegue na árvore à esquerda: Forest > Domains > Seu_Dominio > Group Policy Objects.

Dica: É melhor dar permissão em um objeto específico do que em todos.

2. Delegar o Controle da GPO
Clique na GPO específica que você deseja que o usuário edite.

No painel da direita, clique na aba Delegation (Delegação).

Clique no botão Add... (Adicionar) no canto inferior esquerdo.

Digite o nome do usuário comum e clique em OK.

Na janela de permissões que aparecer, selecione o nível desejado:

Edit settings: O usuário pode alterar as configurações da GPO, mas não pode deletá-la ou mudar quem tem permissão nela.

Edit settings, delete, modify security: O usuário tem controle total sobre esta GPO específica (nível usado para o cenário de GPO Abuse).

Clique em OK.
