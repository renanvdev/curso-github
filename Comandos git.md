# git init
Inicia o git dentro de uma pasta.

# git diff
# git diff --name-only
Exibe as diferenças dentro de determinado commit

# git log
# git log --author 'Renan Vilela'
Exibe o log de todos os commits
#git log --decorate (Exibe aonde está o HEAD) --oneline (Classifica tudo em uma linha)
Para remover um commit, este não pode estar setado como **HEAD**

# git show 77bcb86d7ee8abe074bd741f89ad8c4071013043
Mostra os dados de determinado commit

# git checkout 'index.html' 					                  (Retorna antes da edição de um arquivo)
Remove as alterações dos arquivos no modified status (antes de adicionar ao staged (add))
# git checkout -b nova-branch
Cria uma nova branch

# git branch
Exibe todas as branchs do projeto
# git branch -d nova-branch
Deleta a branch. Após dar merge da branch para o commit, se quiser pode deletar.

# git merge nova-branch
Estando na branch master ou outra que quer mesclar as branchs use este comando.
Todo o conteúdo, mesmo que em arquivos com mesmo nome, são atualizados da nova-branch para a branch alvo.

# git checkout -b testing

# git tag -a 1.0.0 -m 'Finalizado'
# git push origin master -tags
# git tag -d '1.0.0' 						                      (Deleta a tag local)

# git push origin:nome 						                      (Deleta branch ou tag remoto)

-b Criar um novo branch
-u é para crackear, para da proxima vez n precisar fornecer qual o branch

# git reset HEAD index.html 					                  (Retira um arquivo do staged)
# git reset --soft  77bcb86d7ee8abe074bd741f89ad8c4071013043	  (Destroi o commit e volta o arquivo para o staged)
# git reset --mixed 77bcb86d7ee8abe074bd741f89ad8c4071013043	  (Destroi o commit e volta o arquivo para o modified)
# git reset --hard  77bcb86d7ee8abe074bd741f89ad8c4071013043 	  (Destroi tudo)
Retorna ao commit

# git revert + hash do commit que quer voltar :wq
Não altera historico

# git soft / hard reset // Bom para branches separados
Altera o histório, como por ex apagar td o que veio dps do commit que vai voltar com o hard

************* ATENÇÃO
Para subir para o repositório remoto é preciso forçar o push. Isso porque o histórico
que está no repositório local não é o mesmo do remoto, portanto deve-se escrever --force ao
final do push. " **git push origin master --force** "

*****PEGANDO COMMITS ESPECÍFICOS
# git cherry-pick + hash (ex: Pegando só o navbar)