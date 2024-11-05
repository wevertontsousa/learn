# Virtualização

## Sobre
Virtualização é uma tecnologia que permite executar múltiplos OS em um único host físico, possibilitando que o Hospedeiro suporte vários Convidados de forma isolada e com compartilhamento eficiente de recursos como CPU e memória. O processador precisa ter a tecnologia de virtualização habilitada para suportar esse processo. Exemplo de programas que realizam virtualização é o VirtualBox, da Oracle e o Sandbox da Microsoft.

## Virtual Box

### Requisitos
- Configurações de CPU: É necessário entrar no SETUP do PC, acessar as configurações de CPU e definir como Enabled a opção Virtualization. Essa configuração permite que o processador suporte virtualização.
- Download: Baixe o programa Oracle VM VirtualBox compatível com o OS, buscando por "VirtualBox" no Google. Normalmente, o arquivo de instalação terá "hosts" no fim do nome, indicando compatibilidade.

### Instalação
1. Abra o VirtualBox e clique em Novo.
2. Dê um nome oportuno para a máquina virtual.
3. Selecione o Tipo e a Versão do OS que será instalado.
4. É recomendável ajustar a Memória para aproximadamente metade da RAM disponível.
5. Selecione a opção Criar um novo disco rígido virtual agora e escolha o tipo:
    - VDI: recomendável para uso exclusivo no VirtualBox.
    - VHD: recomendável para compatibilidade com outros tipos de máquinas virtuais.
6. Para Armazenamento, o tamanho fixo é mais indicado, e o espaço recomendado é de 32GB (por exemplo, o Windows 10 requer no mínimo 18GB de espaço).

## Sandbox

### Habilitar
1. Pressione a tecla Windows.
2. Pesquise por Windows Features.
3. Clique em Turn Windows features on or off.
4. Selecione a opção Windows Sandbox e ative-a.
5. Após a configuração, crie um arquivo com a extensão .sandbox.
6. Clique duas vezes nesse arquivo para iniciar a Sandbox.
