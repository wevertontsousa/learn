# Ciclo de Requisição-Resposta

## 1º Passo
Um Cliente (programa) é usado para enviar e receber dados na [Internet](internet.md).

Cada tipo de dado requer uma norma, ou protocolo, para ser enviado. Esse protocolo define as regras de comunicação na [Internet](internet.md).

Além dos protocolos, as portas são fundamentais para determinar o tipo de serviço. Cada protocolo tem uma ou mais portas associadas.

Os clientes já implementam o protocolo e a porta que utilizam.

## 2º Passo
O **TCP** do TCP/IP divide os dados em pacotes (partes menores). Cada pacote é numerado para que a ordem de montagem seja preservada no destino.

### 3º Passo
O **IP** do TCP/IP é responsável por inserir o Endereço IP do Remetente e do Destinatário nos pacotes.

Os endereços IP de origem e destino permanecem os mesmos do início ao fim da viagem na rede.

A camada de IP também define a melhor rota até o próximo salto.

### 4º Passo
A **Camada de Enlace** do TCP/IP insere o Endereço MAC nos pacotes. O endereço MAC é atualizado em cada salto com base na rota definida pela camada de IP.

Os pacotes viajam pela [Internet](internet.md) saltando de dispositivo em dispositivo.

Cada dispositivo possui o Endereço MAC do próximo dispositivo na rota, como em um GPS.

O remetente dos dados conhece apenas o próximo dispositivo na rota, e não a rota completa até o destino final.

Sempre que os pacotes chegam ao próximo salto, a camada de IP e Enlace desse dispositivo atualizam o endereço MAC para o próximo dispositivo na rota.

E claro, em cada próximo destino, verifica-se se o endereço MAC do dispositivo atual corresponde ao IP-DESTINATÁRIO. Se corresponder, significa que os pacotes chegaram ao destino final.

Esse processo é conhecido como **salto**.

Exemplo de fluxo desse salto:
dispositivo (casa) ➡️ roteador (casa) ➡️ roteador (provedor) ➡️ roteadores (diversos) ➡️ roteador (destinatário) ➡️ dispositivo (destinatário).

### 5º Passo
A camada de Enlace não envia os dados; ela apenas insere os endereços MAC. Após isso, o **Adaptador de Rede** (Ethernet ou Wi-Fi) converte os dados em sinais físicos.

O **Adaptador de Rede** converte:
- Em **sinais elétricos** para cabo Ethernet.
- Em **ondas de rádio** para Wi-Fi.

Esses sinais físicos carregam os dados até o próximo dispositivo de acordo com o MAC definido (como o roteador/modem da sua casa).

Todos os dispositivos de rede (computador, celular, roteador, impressora, etc.) possuem um **Adaptador de Rede** e precisam realizar essa conversão sempre que enviam dados.

O **Wi-Fi** antes apenas emitia ondas de rádio, enquanto o **Modem** gerenciava a comunicação. Atualmente, o Wi-Fi costuma integrar funções do modem, podendo enviar dados tanto via ondas de rádio quanto por cabo.
