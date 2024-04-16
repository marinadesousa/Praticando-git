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
git rebase -i <referenciaCommit>
~~~

`referenciaCommit` diz respeito à localização do commit que você deseja alterar.

~~~bash
git commit --amend --author="Nome Autor <email@autor>" --no-edit 
~~~

Você também pode usar a flag `--reset-author` no lugar de `--author`, caso seu usuário e email esteja já configurado no Git.

~~~bash
git rebase --continue
~~~

Em seguida o rebase pode continuar o processo.

~~~bash
git push --force
~~~

Por fim, o push forçado atualiza o repositório remoto com a sua nova versão do histórico.