# Git x GitHub

Git é o sistema de versionamento em si, é onde você cria “commits” e pode registrar o histórico de modificações do seu projeto, criar “branches” e, caso algo dê errado, dar “rollback” para uma versão anterior. O github é apenas uma das muitas centrais de repositórios remotos existentes. Outras centrais que você já pode ter ouvido falar são bitbucket ou gitlab, todas elas se encaixam na mesma categoria do github.

## Comandos básicos do Git

### Git add

Este comando adiciona os arquivos solicitados ao ambiente de stage, é uma forma de dizer para o git que você deseja que as modificações daquele arquivo sejam gravadas na próxima remessa. Um exemplo de utilização é: git add . onde o ponto representa todos os arquivos na pasta.

### Git commit

Agora fazemos a gravação em si das modificações, desta forma criamos um snapshot do estado atual do nosso projeto. Uma forma muito usada é o git commit -m “descrição das atualizações do projeto” onde o -m é uma flag que aponta para a mensagem de descrição.

### Git push

Por fim precisamos subir essas modificações no nosso repositório remoto, para isso basta utilizar o comando git push e, se já estiver tudo devidamente configurado, os arquivos serão salvos no repositório remoto correspondente ao seu repositório local!

### Git status

Este comando permite ver quais arquivos estão sendo “rastreados” pelo git e quais modificações já foram enviadas para o stage. É bem útil para quando se tem dúvidas sobre o que está sendo enviado

### Git branch

É usado para verificar todas as branches presentes no repositório. Ao utilizar a flag -r no final do comando é possível ver todas as branches presentes no repositório remoto e se você quiser criar uma nova branch basta utilizar este comando: git branch <branch_name>.

### Git checkout

É o comando utilizado para trocar de branch passando o nome da branch destino no final do comando. Caso a flag -b seja colocada após o “checkout” é possível criar a branch em questão e já trocar para esta imediatamente.

# Como subir um projeto para o GitHub através do Git

- Primeiro vá no github e crie seu repositório. Clique no símbolo de + no topo da tela e depois em New Repository. Preencha um nome e uma descrição para o projeto e clique em Create repository.
- Navegue até a pasta do seu repositório e dentro dela use o comando git init, isso vai transformar a sua pasta em um projeto git (Não vai mudar nada).
- Agora precisamos linkar seu projeto com o seu repositório no github, pra isso você vai usar o comando `git remote add origin https://github.com/user/repo.git.`
- Pronto agora é só subir seus arquivos pro github. Use o comando `git add .` para adicionar todos os arquivos do projeto. Crie um _commit_ inicial `git commit -m "primeiro commit"` e depois dê o push `git push origin master`.
