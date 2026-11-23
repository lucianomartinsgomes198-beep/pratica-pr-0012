# Restauração Clonezilla Lite Server/Cliente
* **Aluno(a):   Robert Rodrigues Rosa Magalhães**
* **Tema:       Backup e Restore**
## 1. Objetivo
* O sistema de Backup e Restauração serve para manter e preservar a integridade dos dados do cliente, mantendo seguros mesmo após uma falha.
## 2. Ferramentas e Cuidados Técnicos
* Ferramentas / Softwares: 
    - Clonezilla Live e GParted Live.
* Segurança / Boas Práticas:
    - Isolar a rede ou o switch durante a clonagem para evitar conflitos com outros servidores DHCP.
    - Conferir cuidadosamente os discos de origem e destino para evitar a perda de dados importantes.
    - Realizar um backup prévio antes de iniciar qualquer procedimento.
    - Verificar a estabilidade da alimentação elétrica dos computadores e do servidor.
    - Garantir que todos os computadores estejam conectados corretamente à rede.
## 3. Passo a Passo
1. Usando o Gparted Live faça a formatação dos dois hds do Computador Servidor, usando a tabela de partição GPT, e formate em ext4. 
2. Usando o Clonezilla Live, no modo device-image, crie uma imagem do disco sda, e salve no disco sdb. 
> Deviceimage > localdev > CTRL_C > sdb1 > no-fsck > "TAB" > "Done" > Beginner > savedisk > Nomear Imagem > z9p > -sgoc > não copiar logs > choose. 
3. Após salvar Imagem do disco sda, use o Clonezilla live no modo Lite Server: 
>  Lite-server > start > both > start-new-dhcpd( use esse modo caso não tenha uma rede DHCP ) > localdev > CTRL_C > sdb1 > no-fsck > "TAB" > "Done" > Beginner > massive-deployment > from-image > restoredisk > sda > -k0 > sim > choose > multicast > clients-to-wait > "coloque a quantidade de máquinas clientes" . 
4. Quando o servidor perguntar "Todos os clientes finalizarão as tarefas de restauração?" 
-  Inicialize todas maquinas clientes usando Boot via rede.
-  Ao aparecer essa tela continue no modo multicast, deixe prosseguir
## 4. Como Validar (Teste Final)
- [ ] Verificar se todas as máquinas clientes receberam corretamente um endereço IP pela rede.
- [ ] Confirmar se os clientes conseguiram estabelecer comunicação com o servidor Clonezilla.
- [ ] Verificar se a restauração multicast foi concluída com sucesso em todas as máquinas clientes.
- [ ] Confirmar se a imagem do sistema operacional foi restaurada corretamente nos discos dos clientes.
- [ ] Verificar se o sistema operacional inicializa normalmente em todas as máquinas restauradas.
- [ ] Confirmar se os dispositivos e configurações essenciais estão funcionando após a restauração.
## Concluído !!!