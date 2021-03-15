# Git Assignment

**INDIVIDUAL**

**Entrega**: 18-Mar-21

## Como entregar
Copie o arquivo em seu repositorio e coloque as respostas nas caixas
Abra uma issue nesse repositório aqui indicando o link para o arquivo no seu repo.

### Entenda o repositorio
Para fazer isso, você terá que baixar [handson.zip] (handson.zip) e descompactá-lo.
A pasta handson é um repositório git. Usando a linha de comando, altere o diretório para "handson /"

As caixas vazias
```

```
representam o conteúdo que você precisa preencher e postar em seu repositório privado

1. Descreva qual é a saída dos seguintes comandos
    -  `git branch` 
    -  `git checkout BRANCH_NAME` (USE THE NAME OF AN EXISTING BRANCH)
    -  `git log --decorate`

```
git branch - Mostra todas as branchs existentes, e assinala com '*' a branch que eu estou

git checkout master - Altera a branch atual para a que eu passei como parametro

git log --decorate - Mostra dos os commits realizados na branch atual

```

2. Tente usar `git log --graph --all`. O que acontece?
```
Mostra a linha do tempo de todos os commits(com uma layout mais "visual"), mostra tambem todas as branchs e sua commits.

```

3. Use `git diff BRANCH_NAME`  para ver as diferenças de um ramo e do ramo atual.
   Sumarize as diferenças do master e do outro ramo.

```
Na master não contem o trecho de código `public void foo() {}` no arquivo A.java

```

4. Escreva uma sequencia de comandos para mesclar o ramo não-master no `master`

```
Caso não esteja na master, execute o seguinte comando:
`git checkout master`
Depois execute o comando:
`git merge BRANCH_NAME`, onde BRANCH_NAME é o nome da branch que você deseja mesclar com a master

```


5. Escreva um comando (ou sequência) para (i) criar um novo ramo chamado `math` (do` master`)
e (ii) mudar para este ramo

```
Caso não esteja na master, execute o seguinte comando:
`git checkout master`
Depois execute o comando que vai criar e ao mesmo tempo mudar para essa branch:
`git checkout -b math`

```
   
6. Edite B.java adicionando o código abaixo ao conteúdo do arquivo
```java
System.out.println("I know math, look:")
System.out.println(2+2)
```

7. Escreva o comando (ou sequencia) para realizar o commit de suas mudanças
```
Use esse comando para adicionar no commit todas as alterações feitas na branch
`git add *`
Agora execute esse comando para finalizar o commit e adicione um comentario para o commit 
git commit -m "comentário"

```

8. Volte para o branch `master` e mude B.java adicionando o seguinte código-fonte (confirme sua mudança para` master`):
```java
System.out.println("Hello World")
```

9. Escreva uma sequência de comando para mesclar o branch `math` em` master` e descreva o que aconteceu
```
`git merge math`
Apos executar o comando, apareceu a mensagem  "CONFLITO (conteúdo): conflito de mesclagem em B.java", apontando conflito entre as branchs

```
   
10. Escreva um conjunto de comandos para abortar a mesclagem
```
Para abortar o merge basta executar o comando:
`git merge --abort`

```
   
11. Agora repita o item 9, mas prossiga com a mesclagem manual (Editando B.java). Todas as funções implementadas são necessárias. Explique o seu procedimento
```
Quando ocorre um conflito, é adicionado marcações sinalizando as alterações puxadas da outra branch, então se voce deseja manter todas as alterações, basta apagar as marcações e realizar um commit.

```

12. Escreva um comando (ou conjunto de comandos) para prosseguir com a mesclagem e atualizar o branch `master`
```
Use o comando para adicionar todas as alterações feitas, que no caso são as aletrações para resolver o conflito
`git add *`
Agora execute o comando para realizar o commit e e atualizar a master
git commit -m "resolve conflicts"

```


