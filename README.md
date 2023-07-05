Repositório com o objetivo de realizar integração do Docker com o Discord gerando alertas quando um container é parado.  
__________________________________________________________________________________________________________________________________
Requisitos  

Host 

Necessário python3 instalado no host.
Necessário criar um virtual environment.
$ python3 -m venv .venv
$ source .venv/bin/activate  
Necessário instalar a biblioteca da API do Docker no virtual environment
$ pip install docker

Obs: Caso deseje conectar com api do docker via socket tcp, editar o arquivo /usr/lib/systemd/system/docker.service e inserir -H tcp://0.0.0.0:2375 na linha ExecStart depois do "-H fd://"

__________________________________________________________________________________________________________________________________

Discord

No Discord é necessário criar um SERVER para envio dos alertas.
Será criado automaticamente um TEXT CHANNEL.
No CHANNEL desejado clique em "EDIT CHANNEL" > Integrations > Webhooks > Crie uma Webhook para os alertas do Docker e será gerada uma Webhook URL.


Referências

https://discord.com/developers/docs/resources/webhook#execute-webhook
https://docker-py.readthedocs.io/en/stable/

Créditos

Aprendizado adquirido na Comunidade Devops by @mateusmuller