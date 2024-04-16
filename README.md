# pratica-git
Repositório para a prática de comandos do Git

~~~bash
git config --global core.editor "code --wait"
~~~

O comando acima define o Visual Studio Code como o editor padrão das mensagens de commit

~~~bash
git commit --allow-empty
~~~ 

O parâmetro --allow-empty permite a criação de um commit vazio, para fins de testes e prática do Git.

~~~bash 
git commit -a
~~~

O parâmetro `-a` adiciona todos os arquivos modificados e não ignorados ao commit atual.

~~~bash
git checkout -b novoBranch
git switch -c novoBranch 
~~~

O parâmetro -b alterna para novoBranch criando o branch. o mesmo acontece com o comando git switch com o parâmetro -c.

~~~bash
git branch -D nomeBranch
git push --delete origin nomeBranch
~~~

Para apagar um branch é preciso primeiro apagá-lo localmente (1º comando) e depois propagar a deleção para o repositório remoto (2º comando).

~~~bash
git log --graph --oneline
~~~

O comando `log` exibe o histórico de commits em detalhes. Com as flags `--graph` e `--oneline`
exibe o histórico em um formato mais compreensível, através de um grafo(grafo?)

### Rebase interativo

Para alterar o autor de um commit, você pode utilizar o rebase interativo e o comando `commit --amend`

~~~bash
git rebase -i <refereciaCommit>
~~~

A referência do commit deve ser sempre para o commit anterior ao commit que deve ser alterado.

No editor de commits, altere a instrução do commit desejado de `pick` para `edit`. Em seguida grave e feche o editor.

O rebase fará uma pausa para que você altere as informações do autor.

~~~bash
git commit --amend --reset-author --no-edit
~~~

Caso você queira especificar o autor, utilize a flag `--author="Nome do Autor <email@autor>"`, nesse exato formato.

Caso seu commit seja vazio, acrescente ainda a flag `--allow-empty`.

Após o reparo do commit, contiue o processo do rebase com o comando abaixo.

~~~bash
git rebase --continue
~~~

Finalmente, **confira o novo histórico 

