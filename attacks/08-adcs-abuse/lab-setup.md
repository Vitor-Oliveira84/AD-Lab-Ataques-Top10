
# Configuração do Laboratório

1. Instalação da Role (Função)
No seu Domain Controller (ou em um servidor membro do domínio):

Abra o Server Manager (Gerenciador de Servidores).
Clique em Manage (Gerenciar) > Add Roles and Features (Adicionar Funções e Recursos).
Avance até Server Roles e marque a caixa:
Active Directory Certificate Services.
Quando abrir a janela de recursos adicionais, clique em Add Features.
Em Role Services (Serviços de Função), selecione obrigatoriamente:
Certification Authority (Obrigatório para ESC1, 2, 5).
Certification Authority Web Enrollment (Obrigatório para ESC8 - NTLM Relay).
Avance e clique em Install.

2. Configuração Pós-Instalação (O Passo Crítico)
Após a instalação, aparecerá uma bandeira amarela com um triângulo no Server Manager. Clique nela e selecione Configure Active Directory Certificate Services:

Credentials: Use uma conta que seja Enterprise Admin.
Role Services: Marque Certification Authority e Certification Authority Web Enrollment.
Setup Type: Escolha Enterprise CA (Isso é fundamental, pois CAs isoladas/Standalone não usam os templates do AD).
CA Type: Escolha Root CA.
Private Key: Selecione Create a new private key.
Cryptography: Pode deixar o padrão (RSA 2048 / SHA256).
CA Name: Dê um nome comum (ex: Lab-CA).
Validity Period: O padrão de 5 anos está ótimo para laboratório.
Clique em Configure.

3. Verificação
Para garantir que tudo está pronto para você criar as vulnerabilidades:

Abra o comando certsrv.msc. Se o ícone da sua CA estiver com um check verde, ela está online.
Tente acessar pelo navegador (de dentro do laboratório): http://localhost/certsrv. Se a página carregar, o ESC8 já está pré-configurado para ser explorado.

Resumo do que você terá agora:
ESC1 e ESC2: Agora você pode abrir o certtmpl.msc e verá os modelos que ensinei a duplicar antes.
ESC5: As propriedades da CA (clicando com o botão direito no nome da CA no console) agora estão disponíveis.
ESC8: O diretório virtual no IIS foi criado e está pronto para ataques de Relay.
```
