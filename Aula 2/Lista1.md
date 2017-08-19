# ** Lista 1 - Git **

### Qual o comando para obter a versão instalada do Git?
git version

### Qual o efeito da execução de cada um dos comandos abaixo?
##### git config -l
Lista todas as configurações que podem ser editadas do git
##### git mv a.txt b.txt
Renomeia o arquivo a.txt para b.txt
##### git reset --hard
Retorna para o último commit, apagando todas as alterações posteriores.
##### git log -27
Mostra os logs dos últimos 27 commits
##### git help
Mostra a ajuda git, listando e descrevendo os comandos mais comuns
##### git help reset
Mostra a ajuda do comando reset em uma página web, com o uso e todos os parâmetros que podem ser chamados
##### git add --all
Adiciona TODOS os arquivos alterados e adicionados/removidos para o index para serem commitados, inclusive untracked
##### git add -u
Se nenhum arquivo for especificado, adiciona todos os arquivos alterados e adicionados/removidos ao index

### O fluxo “clássico” de interação com o Git é algo como “alterar um ou mais arquivos”, “acrescentar essas mudanças para serem contemplados no próximo commit” e, finalmente, executar um “commit”. Quais os comandos necessários para realizar os dois últimos “passos” desse fluxo?
git add -a
git commit "descricao do commit"

### Qual o comando deve ser executado para identificar o que foi alterado desde o último “commit”?
git status

### Em um dado repositório, arquivos simplesmente copiados para lá, ou seja, untracked, podem ser exibidos/identificados com que comando?
git status

### Qual o comando para efetuar um commit?
git commit

### Qual o comando que devemos empregar para descartar mudanças ocorridas no arquivo teste.txt, por exemplo?
git checkout teste.txt

### O que deve ser feito para que um determinado diretório do seu repositório seja ignorado pelo Git? Faça uma busca por .gitignore.
Criar um arquivo .gitignore no seu repositório com o caminho do arquivo/pasta que deseja ignorar especificado.

### O que acontece se o seu repositório local for acidentalmente cd removido?
Quaisquer alterações locais não empurradas para o remoto são perdidas. Você pode clonar o repositório novamente do remoto.

### Como clonar um repositório remoto?
git clone <endereço do repositório remoto>

### Em alguns cenários git log pode produzir extensos resultados. Se houver interesse em visualizar o histórico de um repositório, onde cada mudança é fornecida exatamente em uma única linha, qual o comando que deve ser empregado?
git log --graph --oneline --all --decorate

### Em qual arquivo o Git armazena informações de configuração empregadas por usuário?
Dentro do repositório, no arquivo .git/cofig

### Qual o comando para criar um repositório local?
git init

### Qual o nome do diretório criado pelo Git quando se executa o comando git init?
.git

### Qual o comando para adicionar todos os arquivos modificados? (Aqueles para os quais git status identificam como modified?)
git add .

### O Git faz uso do valor de hash conhecido por SHA1. O que isto significa? Qual o propósito? O que é SHA1?
SHA1 é um algortimo que gera um número hexadecimal de 40 digitos e serve para identificar unicamente cada commit, não existindo 2 commits identicos nunca.

### Qual a palavra para indicar o último commit em vez do valor de hash SHA1 correspondente?
HEAD

### Quando se cria dois arquivos usando um editor de texto qualquer e, na sequência, executamos o comando git add -u, os dois arquivos criados passam de untracked para new file?
Não, pois git add -u ignora arquivos untracked.

### Qual o efeito da execução dos dois comandos abaixo, nesta ordem, em um dado repositório?
##### git reset --soft HEAD~1
Reseta o branch para o último commit, porém mantendo as alterações no arquivos.

##### git reset --hard
Reseta o branch para o último commit, mas sem manter as alterações em nenhum arquivo.

### Após o emprego de um ambiente integrado de desenvolvimento (IDE), é comum a criação de arquivos e diretórios. Qual o comando que podemos empregar para remover arquivos e diretórios untracked?
git clean -f -d

### Qual o nome do arquivo no qual podemos inserir a indicação para o Git de arquivos e diretórios a serem ignorados?
.gitignore

### Quando se cria o arquivo MinhaClasse.class em um dado diretório e desejamos que o Git ignore não apenas este, mas arquivos .class em geral, por todos os membros de uma equipe que estão contribuindo com um dado projeto?
Colocar dentro do arquivo .gitignore a seguinte regra (sem aspas): "*.class"

### No repositório jqueryrepo, criado no passo anterior, qual o efeito do comando  git shortlog -sne?
Exibe uma lista de todos os autores, seus e-mails e o número de commits realizados

### No repositório jqueryrepo, qual o efeito de git remote -v?
Exibe os endereços para puxar e empurrar do repositório remoto

origin  https://github.com/jquery/jquery.git (fetch)
origin  https://github.com/jquery/jquery.git (push)


### Um repositório Git pode ser etiquetado ao longo do tempo. Ou seja, commits específicos podem ser “marcados” ou “etiquetados” para facilitar referências posteriores. Para listar todas as “etiquetas” (tags) estabelecidas para um dado repositório, qual comando deve ser executado?
git tag
 
### Caso um dato repositório retorne muitas “marcas” ou “etiquetas” para o comando git tag, como retornar apenas aquelas que atendem a determinado padrão, por exemplo, iniciadas por 2.0?
git tag --list 2.0*
 
### Qual o efeito do comando git tag -a 3.4-gold -m “minha versão ouro”?
Cria uma tag 3.4-gold com a descrição 'minha versão ouro'.

### Após executado o comando acima, qual o efeito de git show 3.4-gold?
Exibe o commit e as alterações feita no commit da tag.

### O que o comando git push origin 3.4-gold teria como efeito?
Empurra a tag criada localmente para o repositório remoto

### Após executar um commit, qual o efeito de git commit --amend?
Adicionar alterações recentes ao ultimo commit ao invés de criar outro commit. Também serve para somente editar a mensagem do commit.

### Após executar git add x.txt, qual o efeito de git reset HEAD x.txt?
O arquivo continua modificado, mas não está mais staged

### Após alterar o conteúdo de um arquivo committed em passo anterior, qual o efeito do comando git checkout -- a.txt?
O arquivo volta ao estado em que estava no último commit, perdendo as alterações.

### Qual a diferença entre os comandos git reset HEAD x.txt e git checkout -- a.txt?
Um deles tira o arquivo alterado da staging area e o outro remove as alterações feitas no arquivo.