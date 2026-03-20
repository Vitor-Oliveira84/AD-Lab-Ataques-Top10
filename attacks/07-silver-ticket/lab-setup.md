
# Configuração do Laboratório

Para forjar um Silver Ticket, você precisa de:
Hash NTLM do alvo: Pode ser o hash de uma conta de serviço (como o svc_sql que criamos no Kerberoasting) ou o hash da conta de um computador (ex: SERVER01$).
SID do Domínio.
Nome do Serviço (SPN): Ex: cifs (para arquivos), http (para web), mssql (para banco).
Nome do Servidor Alvo: Ex: server01.lab.local.
