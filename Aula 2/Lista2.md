# ** Lista 2 - Git **

### Qual o comando para que as “marcas” ou tags sejam enviadas para o repositório remoto? (um simples git push não produz este efeito)
git push --tags

### Qual o nome do branch padrão do Git?
master

### O que o comando git branch <branchname> realiza?
cria um novo branch local

### Como criar um branch a partir de um commit específico?
git branch <nomebranch> <id do commit>

### Em um repositório, qual o efeito do comando git branch erro1234?
Cria o branch erro1234

### Qual o comando para se alternar para um branch de nome experimento2?
git checkout experimento2

### Em um repositório com dois branches, b1 e b2, onde b1 é o corrente, qual o efeito do comando git branch?
Lista o branch b1 e b2 (todos os branches existentes)

### O que o comando git checkout -b novobranch faz?
Cria o branch novobranch e alterna para trabalhar nele

### Qual a função do comando git branch -d teste?
Deleta o branch local teste.

### Questão:
#### Durante o desenvolvimento de um software é comum, por exemplo, utilizar um novo recurso por meio de experimentação. Talvez uma nova tecnologia, uma nova biblioteca que pode ser útil ao que está em desenvolvimento, ou até mesmo uma nova versão de um produto já empregado. Para que o uso deste novo recurso não interfira com o que é considerado pronto, um branch pode ser criado para a experimentação. Código que for criado para a experimentação existirá apenas no branch criado. Se eventualmente o experimento demonstrar um resultado satisfatório, as alterações realizadas no branch poderão ser incorporadas no que é considerado pronto, ou seja, no branch principal (master). Esta última ação é conhecida por merge. Neste item, apresente uma sequência de comandos que simula um caso simples de criação e uso seguido de merge empregando um branch para ilustrar uma experimentação conforme acima. A sequência deve incluir, obrigatoriamente: (a) criação de um ou mais branches; (b) chaveamento para pelo menos dois branches e (c) merge. Para simular alteração em um arquivo, basta simplesmente fornecer algo como Arquivo <nome> é alterado. O que foi fornecido em negrito representa uma ação que altera um arquivo cujo nome é fornecido entre o sinal de menor e o de maior.

git checkout - b branch1

**Arquivo <oi.txt> é alterado.**

git commit -a "oi"

git checkout master

git checkout -b branch2

**Arquivo <tchau.txt> é alterado.**

git commit -a "tchau"

git checkout master

git merge branch1

git branch -d branch1

git merge branch2

git branch -d branch2

