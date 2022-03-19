# GIT - Versionamento de Código
- Controle de versão de sistema distribuído

## Tópicos Fundamentais

### SHA-1
- Algoritmo de encriptação
- A encriptação gera um conjunto de 40 caracteres, que serve como identificação
- Qualquer mudança feita em um arquivo, irá gerar um SHA-1 diferente

### Objetos Internos do GIT
- blob: contém metadados dos arquivos
- Tree: armazena blobs e tem os metadados dessa árvore
- Commit: aponta para uma árvore(tree), para o ultimo commit, para o autor e para a mensagem
  - Também possui a geração de um SHA-1

## Comandos
- <code>git init</code> : inicializar o repositório git
- <code>git add .</code>: adicionar arquivos
- <code>git commit -m "descrição do commit"</code>: criar um commit
- <code>git status</code>: mostra o status dos arquivos
- <code>git remote add origin [URL-repositório]</code>: apontar o repositório local para um repositório remoto
- <code>git push [origin master]</code>: enviar o repositório local para o repositório remoto
- <code>git pull [origin master]</code>: pegar os arquivos do repositório remoto para o repositório local

### Resolver conflitos
- Conflito de merge: GitHub tenta juntar duas alterações em uma mesma linha
  - Ele não irá alterar, indicará para que você escolha o que quer manter ou excluir e ai sim enviar

## Ciclo de Vida
### Untracked
- Não rastreado pelo git
- Para mover para _staged_, é usado o comando git add

### Staged
- Arquivos aqui, estão se preparando para fazerem parte de um commit

### Ambiente de Desenvolvimento/ Computador Local
- Working Directory: o repositório de trabalho
- Staging Area: área onde os arquivos esperam por um commit
- Local Repository: após um commit, os arquivos começam a fazer parte desse repositório local