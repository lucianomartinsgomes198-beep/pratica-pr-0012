# Clonagem de disco em Máquina virtual com clonezilla

* Aluno(a):bernardo augusto da silva reis
* Tema: Backup e Restore

## 1. Objetivo
 a clonagem de disco serve para criar uma cópia em outro ssd ou hd, duplicando sistema operacional,programas,configurações,etc.

## 2. Ferramentas e Cuidados Técnicos
* Ferramentas / Softwares: será utilizado o clonezilla.
* Segurança / Boas Práticas:certifique qual o disco de origem  e qual é o destino para não sobescrever dados, e confira também se o novo disco tem capacidade igual ou superior ao original e selecione a opção device-device para clonar corretamente.


# passo a passo
1. coloque a imagem iso do clonezilla adicione novo disco com memoria suficiente para clonagem.
2. 
   realize o processo de clonagem pelo clonezilla e ao final vá para o linux mint
   adicione um disco extra com espaço suficiente para clonagem.

 3. não  apague o disco original antes validar a clonagem, desconecte o disco original nas configurações da vm e teste o boot,pois se algo falhar os seus dados ainda continuam intactos.


## 4. Como Validar (Teste Final)
-  A máquina Virtual iniciou (fez o boot) normalmente no linux mint apenas com disco que foi  clonado.
-  Todos os arquivos ,configurações e programas do sistema original estão persentes e funcionado no novo disco.

