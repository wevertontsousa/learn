<img
    src="https://www.dinamcorp.com.br/Arquivos/posts/03052016105453_internet-54.jpg"
    style="height: 200px; width: 100dvw; object-fit: cover;"
/>


# Rede

É um conjunto de dispositivos (como computadores, smartphones, servidores, roteadores e switches) conectados entre si para compartilhar dados. Redes podem ser pequenas, como uma __rede doméstica__, ou grandes, como as __redes corporativas__.


## Internet

É uma __Rede__ global que conecta milhões de redes menores no mundo todo. Ela permite que dispositivos em redes diferentes se comuniquem. Basicamente, é a "rede das redes".

Existem __Serviços__ comuns realizados na Internet, para que essa comunicação ocorra de forma correta, alguns deles são: __Web__, E-mail e Streamings.

Além dos serviços __Portas__ também tem um papel importante nessa comunicação.


### ARPANET (Advanced Research Projects Agency Network)

Primeira rede de __Internet__, criada em 1969, tinha o objetivo de interligar laboratórios de pesquisa e departamentos de defesa nos Estados Unidos. Ela usava o NCP (Network Control Protocol).

O TCP (Transmission Control Protocol) surgiu em 1974, e em 1983 a ARPANET mudou do NCP para TCP.

Até o final da década de 80 já tinham prontos TCP, IP e UDP.

No final de 1970 a ISO (International Standard Organization) propôs o Modelo OSI, que só foi publicado em 1984.


## Serviços

Referem-se aos recursos e funcionalidades que a _rede de Internet_ disponibiliza para os usuários. Em termos gerais, serviços em uma rede são aplicativos e __protocolos__ que permitem a troca de informações e a realização de tarefas específicas. Além disse cada serviço usa uma __porta__ específica para enviar e receber os dados.


### Web (World Wide Web, WWW ou www)

Serviço para acessar páginas e sites acessíveis pela Internet, que usamos para ver conteúdos (como textos, imagens e vídeos).

Navegadores como Edge, Chrome ou Safari oferecem esse serviço para solicitar e exibir conteúdo da Web.

A Web é projetada para ser interativa e __navegar__ entre páginas conectadas por links.


### E-mail

Serviço para envio de __mensagens__ pela Internet, que usamos para ver conteúdos (como textos e anexos).

Programas como G-mail, ou Outlook oferecem esse serviço para solicitar e exibir E-mails.


### Streaming

Serviço para consumir dados contínuos pela Internet, que usamos para __assistir__ vídeos e __ouvir__ músicas em __tempo real__, sem precisar baixar.


## Portas

Porta é um canal de comunicação associado a um __protocolo__ ou _processo_ específico que escuta e responde dados.

| Porta | Protocolo de Transporte | Protocolo de Aplicação      | Descrição                             |
|-------|--------------------------|-----------------------------|---------------------------------------|
| 20    | TCP                      | FTP (dados)                 | Transferência de arquivos (dados)     |
| 21    | TCP                      | FTP (controle)              | Transferência de arquivos (controle)  |
| 22    | TCP                      | SSH                         | Acesso remoto seguro                  |
| 23    | TCP                      | Telnet                      | Acesso remoto não seguro              |
| 25    | TCP                      | SMTP                        | Envio de e-mails                      |
| 53    | TCP/UDP                  | DNS                         | Resolução de nomes de domínio         |
| 80    | TCP                      | HTTP                        | Navegação web                         |
| 110   | TCP                      | POP3                        | Recebimento de e-mails                |
| 143   | TCP                      | IMAP                        | Recebimento de e-mails                |
| 443   | TCP                      | HTTPS                       | Navegação web segura                  |
| 465   | TCP                      | SMTPS                       | Envio de e-mails seguro               |
| 993   | TCP                      | IMAPS                       | Recebimento de e-mails seguro         |
| 995   | TCP                      | POP3S                       | Recebimento de e-mails seguro         |
| 1194  | UDP                      | OpenVPN                     | VPNs seguras                          |
| 1433  | TCP                      | MS SQL Server               | Banco de dados Microsoft SQL Server   |
| 1521  | TCP                      | Oracle                      | Banco de dados Oracle                 |
| 3306  | TCP                      | MySQL                       | Banco de dados MySQL                  |
| 3389  | TCP                      | RDP                         | Acesso remoto Windows                 |
| 5432  | TCP                      | PostgreSQL                  | Banco de dados PostgreSQL             |
| 5900  | TCP                      | VNC                         | Controle remoto                       |
| 6379  | TCP                      | Redis                       | Banco de dados Redis                  |
| 8080  | TCP                      | HTTP (alternativo)          | Alternativa para HTTP                 |
| 8443  | TCP                      | HTTPS (alternativo)         | Alternativa para HTTPS                |
| 1935  | TCP                      | RTMP                        | Streaming de vídeo                    |
| 554   | TCP/UDP                  | RTSP                        | Streaming de áudio e vídeo            |
| 1755  | TCP/UDP                  | MMS                         | Streaming de mídia Microsoft          |
| 3478  | TCP/UDP                  | STUN                        | Streaming e chamadas de vídeo         |
| 8081  | TCP                      | HTTP (admin)                | Administração de serviços HTTP        |
| 5000  | TCP                      | RTP                         | Protocolo de transmissão de mídia     |
| 5001  | TCP                      | RTP (alternativo)           | Alternativa para RTP                  |


## Protocolos

São _regras_ a serem cumpridas para uma determinada ação na __Internet__.

Além de regra pode ser classificado como: _modelo conceitual_; _normas_; _especificação_; _contrato_; _abstração_.


### HTTP (Hyper Text Transfer Protocol)

![Requisição HTTP](https://mdn.github.io/shared-assets/images/diagrams/http/overview/http-request.svg)
![Resposta HTTP](https://mdn.github.io/shared-assets/images/diagrams/http/overview/http-response.svg)
![HTTP](https://i0.wp.com/www.diegomacedo.com.br/wp-content/uploads/2016/08/Mapa-Mental-Protocolo-HTTP.png)

Caminho:
- `https://<Domínio>:<Porta>/<Recurso>`
- `https://<Domínio>:<Porta>/<Recurso>/<Id>`
- `https://<Domínio>:<Porta>/<Recurso>/<Id>?<filtros>`
- `http://localhost:8080/api/v1/user/1/ordes?orderBy=total,DESC`

Métodos (Requisição):
- `POST`: criar (salvar)
- `GET`: listar um ou todos
- `PUT`: substituir
- `PATCH`: atualizar parcialmente
- `DELETE`: remover

Códigos e Mensagem de Status (Resposta):
- `200 OK`: retorna o recurso
- `202 Accepted`: retorna o recurso de forma assíncrona
- `204 No Content`: retorna `null`

`GET`, `PUT`, `PATCH` e `DELETE` ➡️ `200 OK` ou `204 OK`.
`POST` ➡️ `201 OK` ou `202 OK` ou `204 OK`.
