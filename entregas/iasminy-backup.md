# Backup e Restore de Estações com Clonezilla

* **Aluno(a):** Iasminy Vitoria Caetano Rodrigues 
* **Tema:** Procedimento Técnico De Backup/Restore da UC 3.

## 1. Objetivo
Documenta o procedimento de backup e restore da UC3 usando Clonezila, para garantir que dá pra recuperar o sistema rapidamente se der falha e assim, manter todos os PCs padronizados. 

## 2. Ferramentas e Cuidados Técnicos
* Clonezilla live no arquivo .ISO, HD interno de tamanho igual ou superior.
* Cuidados especificos de backup, usar nobreak pra não desliga durante o procedimento, conferir espaço no HD externo antes e validar a imagem depois.

## 3. Passo a Passo
1. Ligar o PC Matriz pela imagem do Clonezila, escolher device-image e depois local_dev para escolher o HD externo.
2. Escolher savedisk para criar a imgem completa do disco e salvá-la em /home/partimag.
3. Exemplo:/home/partimag/backup-matriz-2026

## 4. Restaurar a imagem 
1. Ligar o PC  que vai receber a restauração pela imagem do Clonezilla, escolher device-image e depois local_dev para escolher o HD externo ond está a imagem.
2. Escolher restoredisk para restaurar a imagem completa do disco.
3. Escolher a imagem correta, ex: backup-matriz-2026, e depois escolher o disco de destino com atenção para não apagar o disco errado 
4. Confirma a restauração e aguardar termina. Quando aparecer a mensagem de concluído no Clonezilla, desligar o PC e ligá-lo novamente para validar seo sistema iniciou normalmente 

## 5. Como Validar (Teste Final)
- [ ] PC ligou normal, sem tela azul ou erro de boot.
- [ ] Entrou no S.O. e arquivos de matriz aparecendo. 
- [ ] Todos os programas e configurações 