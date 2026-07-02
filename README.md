# Guia de comandos Git

# Foco no ambiente de terminal
Interface de Linha de Comando (CLI) que permite que você interaja diretamente com o sistema operacional do seu computador através de comandos.

## Atalhos
⚠️**Atenção (caminhos com espaços)** - Envolva caminhos que contenham espaços entre aspas
Ex: `cd "C:\Program Files\Meu App"`

**Seta para cima e para baixo no terminal** - revisita o histórico de comandos digitados anteriormente no terminal, possibilitando uma execução mais rápida de comandos.

**Tab para auto-complete** - Pode-se usar o atalho Tab para completar automaticamente o nome de alguma pasta ou algum comando

**Ctrl+L**  - Limpa o terminal

## Comandos (CMD)
- `dir` - Listar tudo que está no seu diretório (pasta) atual, dependendo do terminal ele pode mostrar o tipo de arquivo com alguma cor diferente. O parâmetro `/ah` exibe arquivos e diretórios ocultos
	- Ex: `dir`
- `cls` - Limpa o terminal
	- Ex: `cls`
- `cd` - Mudar de um diretório para outro.
	- Ex: `cd diretorio`
	Pode ser usado com `..` para voltar um diretório anterior
	- Ex: `cd ..`
- `del` - Deleta um arquivo
	- Ex: `del arquivo.txt`
- `rmdir` - Deleta um diretório.
	- Ex: `rmdir diretorio`
- `mkdir` - Cria um novo diretório.
	- Ex: `mkdir novadir`
- `move` - Move arquivos/diretórios
	 - Ex: `move arquivo.txt C:\NovaPasta\`
## Comandos (Bash)
- `ls` Listar tudo que está no seu diretório atual, dependendo do terminal ele pode mostrar diferentes tipos de arquivos com cores diferentes. O parâmetro `-a` exibe arquivos e diretórios ocultos
	- Ex: `ls`
-  `clear` Limpa o terminal
	-  Ex: `clear`
- `cd` - Mudar de um diretório para outro. Pode ser usado com `..` para voltar um diretório anterior
	Ex: `cd diretorio`
- `rm` - Deleta um arquivo.
	Ex: `rm arquivo.txt`
- `rmdir` - Deleta um diretório.
	Ex: `rmdir diretorio`
- `mkdir` - Cria um novo diretório.
	Ex: `mkdir novadir`
- `mv` - Move arquivos/diretórios ou renomear arquivos/diretórios. Use o parâmetro `-i` para que o terminal pergunte antes de sobrescrever algo com o mesmo nome. 
	- Ex (movendo arquivo): `mv -i arquivo.txt /home/usuario/Documentos/`
	- Ex (renomeando arquivo): `mv -i foto_antiga.jpg foto_nova.jpg`
- `nano` - Abre o editor de texto do terminal linux, pode ser usado para ver e editar o conteúdo de um arquivo. (Se não houver arquivo com o nome, um novo arquivo pode ser salvo com esse nome após fechar o editor)
	Ex: `nano lista.txt`
- `touch` - Cria um arquivo vazio.
	- Ex: `touch novo_arquivo.txt`
- `cp` - Copia arquivos e diretórios.
	- Ex: `cp arquivo.txt copia.txt`
 
 <hr>
<br>

# O que é controle de versão?

O **controle de versão** é o processo de registrar, acompanhar e gerenciar todas as alterações realizadas em um arquivo ou projeto ao longo do tempo. Ele permite que desenvolvedores mantenham um histórico completo das modificações, identifiquem quem realizou cada alteração e recuperem versões anteriores quando necessário.

Em projetos de desenvolvimento de software, o controle de versão é essencial para organizar o trabalho em equipe, evitando que alterações sejam perdidas ou sobrescritas. Ferramentas como o **Git** permitem que vários desenvolvedores trabalhem simultaneamente no mesmo projeto por meio de *branches*, integrando posteriormente as alterações de forma segura.

## Principais benefícios

- Mantém o histórico completo das alterações.
- Facilita o trabalho colaborativo entre equipes.
- Permite criar diferentes versões do projeto por meio de *branches*.
- Possibilita restaurar versões anteriores quando necessário.
- Identifica quem realizou cada alteração e quando ela foi feita.

## Exemplo prático

Imagine que uma equipe está desenvolvendo um sistema. Um integrante cria uma nova funcionalidade enquanto outro corrige um erro. Com o controle de versão, cada um trabalha em sua própria *branch*, registrando suas alterações sem interferir no trabalho do outro. Depois, essas alterações podem ser reunidas no projeto principal.

## Tipos de controle de versão

<p align="center">
  <img src="assets/tipo-controle-de-versao.png" width="100%">
</p>

>Os sistemas de controle de versão podem ser classificados em dois tipos principais: **centralizado** e **distribuído**.

## 1. Controle de versão centralizado (CVCS)

> No controle de versão centralizado, existe um **único servidor central** que armazena todos os arquivos e o histórico de alterações. Os desenvolvedores acessam esse servidor para enviar e receber modificações.

### Características

- Um único repositório central.
- Dependência do servidor para acessar o histórico.
- Facilita o gerenciamento por um administrador.
- Se o servidor ficar indisponível, o trabalho da equipe pode ser interrompido.

### Exemplos

- CVS (Concurrent Versions System)
- Subversion (SVN)

---

## 2. Controle de versão distribuído (DVCS)

> No controle de versão distribuído, cada desenvolvedor possui uma **cópia completa do repositório**, incluindo todo o histórico de alterações. Assim, é possível trabalhar mesmo sem conexão com a internet e sincronizar as mudanças posteriormente.

### Características

- Cada desenvolvedor possui um repositório completo.
- Permite trabalhar offline.
- Maior segurança, pois existem várias cópias do histórico.
- Facilita o trabalho colaborativo.

### Exemplos

- Git
- Mercurial
- Bazaar

---

## Comparação

| Controle Centralizado | Controle Distribuído |
|------------------------|----------------------|
| Possui um único servidor central. | Cada desenvolvedor possui uma cópia completa do repositório. |
| Depende do servidor para acessar o histórico. | Permite trabalhar offline. |
| Maior risco caso o servidor falhe. | Maior segurança, pois existem várias cópias do projeto. |
| Exemplo: SVN. | Exemplo: Git. |

## Qual tipo o Git utiliza?

O **Git** é um **sistema de controle de versão distribuído (DVCS)**. Isso significa que cada desenvolvedor possui uma cópia completa do repositório em seu computador, podendo registrar alterações, criar *branches* e consultar o histórico mesmo sem acesso à internet.

> **Resumo:** Os sistemas de controle de versão podem ser **centralizados** ou **distribuídos**. O Git pertence à categoria dos sistemas distribuídos, oferecendo maior flexibilidade, segurança e colaboração entre desenvolvedores.

## Resumo

> **Controle de versão** é o processo de registrar e gerenciar as alterações realizadas em um projeto, permitindo acompanhar seu histórico, colaborar com outras pessoas e recuperar versões anteriores de forma segura.

### Exemplo de fluxo

```text
Versão 1 → Versão 2 → Versão 3 → Versão 4
     │          │          │
 Histórico de todas as alterações
```

 <hr>
<br>
<br>
 
# O que é Git ?

<p align="center">
  <img src="assets/git-logo.jpg" width="250" alt="Logo Git">
</p>

O **Git** é um sistema de controle de versão distribuído, criado por **Linus Torvalds** em 2005. Ele permite registrar, acompanhar e gerenciar as alterações realizadas em arquivos e projetos ao longo do tempo.

Com o Git, é possível manter um histórico completo das modificações, trabalhar em diferentes versões do mesmo projeto por meio de *branches* e colaborar com outros desenvolvedores de forma organizada e segura.

Como é um sistema distribuído, cada desenvolvedor possui uma cópia completa do repositório em seu computador, incluindo todo o histórico de versões.

---

## Principais funcionalidades

| Funcionalidade | Descrição |
|----------------|-----------|
| Controle de versões | Mantém o histórico das alterações do projeto. |
| Branches | Permite desenvolver funcionalidades separadamente. |
| Commits | Registra as alterações realizadas. |
| Merge | Une alterações de diferentes branches. |
| Reversão | Recupera versões anteriores do projeto. |
| Colaboração | Facilita o trabalho em equipe. |

## Exemplo de uso

Imagine que uma equipe está desenvolvendo um site. Cada integrante cria uma *branch* para desenvolver uma funcionalidade específica, como a página inicial ou o sistema de login. Após concluir o desenvolvimento, as alterações são registradas com um *commit* e, posteriormente, integradas à branch principal.

### Fluxo básico do Git

```text
git clone ou git init
        │
        ▼
Criar uma branch
        │
        ▼
Editar arquivos
        │
        ▼
git add
        │
        ▼
git commit
        │
        ▼
git push
```

## Vantagens do Git

- Histórico completo de alterações.
- Trabalho colaborativo eficiente.
- Facilidade para identificar e corrigir erros.
- Segurança por meio do controle de versões.
- Organização do desenvolvimento em equipes.

> 💡 **Importante:** O Git funciona localmente no computador do desenvolvedor. Para compartilhar o projeto com outras pessoas, normalmente utiliza-se o GitHub.

## Resumo

> **Git** é um sistema de controle de versão que permite registrar, acompanhar e gerenciar as alterações realizadas em um projeto, facilitando o desenvolvimento individual e colaborativo.
 <hr>
<br>

 ## Instalando e configurando o Git

<p align="center">
  <img src="assets/config-git.png" alt="Git" width="100%">
</p>

Caso o Git ainda não esteja instalado em seu computador:

1. Acesse:

```text
https://git-scm.com/downloads
```

2. Baixe a versão correspondente ao seu sistema operacional;
3. Execute a instalação mantendo as configurações padrão.

---

## Configurando o Git

Após instalar o Git, abra o terminal (Prompt de Comando, PowerShell ou Terminal do VS Code) e execute:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@email.com"
```

Exemplo:

```bash
git config --global user.name "Mariana Monteiro"
git config --global user.email "mariana@email.com"
```

Para verificar as configurações:

```bash
git config --global --list
```

Ou consultar cada informação individualmente:

```bash
git config --global user.name
git config --global user.email
```

---

## Fazendo login no GitHub pelo VS Code

<p align="center">
  <img src="assets/vscode.jpg" alt="Vscode" width="200%">
</p>

1. Abra o Visual Studio Code;
2. Clique no ícone de **Conta**;
3. Selecione **Sign in with GitHub**;
4. Autorize o acesso no navegador.

Após o login, será possível:

* Clonar repositórios;
* Criar branches;
* Fazer commits;
* Enviar alterações para o GitHub (`git push`);
* Criar Pull Requests.

---

### Dica:

Antes de iniciar qualquer projeto, confirme se o Git está configurado corretamente:

```bash
git config --global user.name
git config --global user.email
```

> Essas informações serão utilizadas para identificar a autoria de todos os commits realizados no repositório.

---

## Arquivos Especiais de Configuração

1. `.gitignore`
é um arquivo de texto onde você lista explicitamente todos os arquivos, formatos ou pastas que o Git **deve ignorar**. Tudo o que estiver documentando aqui não será rastreado pelo Git e não irá para o repositório
	
	> **Para que serve:** Evitar o envio de arquivos gerados automaticamente (como as pastas e arquivo`.env, node_modules, dist` e `build`) e arquivos do própio sistema operacional (como`.DS_Store` no Mac)
2. `.env`
é o arquivo utilizado para armazenar as **variáveis de ambiente** do seu projeto.
	
	> **Para que serve:** Ele guarda dados sensíveis e configurações específicas da sua máquina local, como senhas de bancos de dados, chaves de APIs privadas e portas de servidores.
		**Atenção**: O arquivo `.env` **NUNCA deve ser enviado para o Git**. Por conter dados secretos, o nome `.env` deve ser obrigatoriamente adicionado dentro do seu arquivo `.gitignore`.

---

## Instalação e Configuração
Instalar o Git na sua máquina é muito simples. Basta acessar o site: https://git-scm.com/install/windows e realizar o download de acordo com seu SO.

> Após concluir a instalação, você terá tanto uma versão command line (linha de comando, incluindo um cliente SSH que será útil depois) e uma GUI padrão.

A primeira coisa que você deve fazer quando instalar o Git é definir o seu nome de usuário e endereço de e-mail. Isso é importante porque todos os commits no Git utilizam essas informações, e está imutavelmente anexado nos commits que você realiza.

`git config --global user.name "Fulano De Tal"`
`git config --global user.email "fulanodetal@exemplo.com"`

> Lembrando, você precisa fazer isso uma vez caso passe a opção `--global,` pois o Git sempre usará essa informação para qualquer coisa que você faça nesse sistema. Caso você queira sobrepor estas com um nome ou endereço de e-mail diferentes para projetos especifico, você pode executar a opção `--global` quando estiver no próprio projeto.

Se você precisar de ajuda ao usar o Git, existem três maneiras de obter a ajuda para qualquer um dos comandos Git.

- `git help <comando>`
- `git <comando> --help`
- `man git <comando>`

Extra: O comando principal para listar a lista de comandos disponíveis no Git é: `git help -a`

---

## Verificação
Depois de instalar e configurar o Git, É importante garantir que o terminal do seu sistema operacional consegue reconhecê-lo. Para isso, basta abrir o seu Terminal(Prompt de Comando, Powershell ou Git Bash) e digitar um dos comandos abaixo:

`git --version`

Se tudo estiver correto, o terminal retornará o texto indicando a Versão do Git instalada na sua máquina, algo parecido com:

`git version 2.55.0.windows.1`

Se o terminal retornar uma mensagem de erro como "*commando not found*" ou "*Não é reconhecido como um comando interno*", significa que o Git não foi instalado corretamente ou que o caminho dele não foi adicionado as variáveis de ambiente do seu sistema.

# Comandos Git 

São ferramentas de linha de comando essenciais para o controle de versão distribuído, permitindo gerenciar alterações no código-fonte, colaborar com equipes e manter um histórico detalhado do projeto.

<p align="center">
  <img src="assets/principais-comandos-git.jpg" alt="comandos Git" width="100%">
</p>

> Nesta página, será explicado cada comando passo a passo para determinados contextos.

## Criando o Projeto
Você pode obter um projeto Git fazendo uso de um projeto ou diretório existente e o importando para o Git ou clonando um repositório Git existente a partir de outro servidor (Github).

---

## Inicializando Repositório em um Diretório Existente
Caso você esteja iniciando o monitoramento de um projeto existente com Git, você precisa ir para o diretório do projeto e digitar: 

```bash
git status
```
Isso cria um novo subdiretório chamado `.git` que contem todos os arquivos necessários de seu repositório, um esqueleto de repositório Git.

## Criando o arquivo .gitignore

O arquivo `.gitignore` é utilizado para informar ao Git quais arquivos e pastas **não devem ser monitorados ou enviados para o repositório**.

### 1. Criar o arquivo

```bash
touch .gitignore
```

**Finalidade:** Cria um arquivo vazio chamado `.gitignore` na pasta atual do projeto.

> **Observação:** O comando `touch` é utilizado em sistemas Linux e macOS. No Windows, você pode criar o arquivo manualmente pelo VS Code ou pelo Explorador de Arquivos.

---

### 2. Adicionar o arquivo ao Git

```bash
git add .gitignore
```

**Finalidade:** Adiciona o arquivo `.gitignore` à área de preparação (*Staging Area*), indicando que ele fará parte do próximo commit.

---

### 3. Salvar o arquivo no histórico do projeto

```bash
git commit -m "Adiciona arquivo .gitignore"
```

**Finalidade:** Cria um novo commit contendo o arquivo `.gitignore`.

> A opção `-m` permite informar uma mensagem descrevendo a alteração realizada.

Exemplo:

```bash
git commit -m "Adiciona arquivo .gitignore"
```

### Exemplo completo

```bash
touch .gitignore
git add .gitignore
git commit -m "Adiciona arquivo .gitignore"
```

> Após esses comandos, o arquivo `.gitignore` passa a fazer parte do histórico do projeto e o Git passa a ignorar os arquivos e pastas especificados nele.

Caso você queira começar a controlar o versionamento dos arquivos existentes, você provavelmente deve começar a monitorar esses arquivos e fazer um commit inicial. Você pode realizar isso com poucos comandos.

```bash
touch .gitignore
git add .gitignore
git commit -m "Mensagem"
```
> Agora, você possui um repositório Git com arquivos monitorados e um commit inicial.

# Clonando um Repositório
Você pode clonar um repositório com `git clone <URL>`. Por exemplo, caso você queira clonar o repositório do curso de Git e Github do Gustavo Guanabara, você pode executar da seguinte forma:
```bash
git clone https://github.com/gustavoguanabara/git-github.git
```
> Quando um repositório é inicialmente clonado, todos os seus arquivos estarão monitorados e inalterados porque você simplesmente os obteve e ainda não os editou.

# Registrando Alterações
Conforme você edita os arquivos do seu clone local de um repositório, o Git passa a vê-los como modificados, porque você os alterou desde seu ultimo commit. Você seleciona esses arquivos modificados e então faz o commit de todas as alterações selecionadas e ao longo do projeto esse ciclo passa a se repetir.

Para passar a monitorar um novo arquivo, use o comando `git add`. Para monitorar o arquivo README, você pode rodar isso:
```bash
git add README
```
Caso queira adicionar todas as modificações feitas no projeto use o comando:
```bash
git add .
```

Se você rodar o comando `git status`, você verá quer o seu arquivo `README` agora está sendo monitorado. Os arquivos monitorados faram parte do commit.

 <hr>
<br>

## Verificando o Status
A principal ferramenta utilizada para determinar quais arquivos estão em quais estados é o comando:
```bash
git status
```
> O comando mostra em qual branch você se encontra. Vamos dizer que você adicione um novo arquivo em seu projeto, um simples arquivo README. 

Caso o arquivo não existe e você execute `git status`, você verá o arquivo não monitorado dessa forma:

`#On branch master`

`#Untracked files:`

`# (use "gid add {files}..." to include in what will be commited)`

`#`

`#README`

`nothing added to commit but untracked files presente (use"git add" to track)`

Pode ver que o seu novo arquivo `README` não está sendo monitorado, pois está listado sob o cabeçalho "**Untracked files**" na saída do comando status. Não monitorado significa basicamente que o Git está vendo um arquivo que não existia na ultima captura (commit).

> O Git não vai inclui-lo nas suas capturas de commit até que você o diga explicitamente que assim o faça. Ele faz isso para que você não inclua acidentalmente arquivos binários gerados, ou outros arquivos que você não tem a intenção de incluir.

## Verificando Mudanças
Se o comando `git status` for muito vago, você quer saber exatamente o que você alterou, não apenas quais arquivos foram alterados. Você pode utilizar o comando:
```bash
git diff
```
Apesar do comando `git status` responder essas duas perguntas de maneira geral, o `git diff` mostra as linhas exatas que foram adicionadas e removidas, o patch, por assim dizer.

Se você quer ver o que selecionou que irá no seu próximo commit, pode utilizar:
```bash
git diff --cached`
```

# Commits
> Armazena o conteúdo atual do índice em um novo commit, juntamente com uma mensagem de registro do usuário que descreve as mudanças.

- Se usa o commit depois de já ter feito o `git add`, para fazer o commit:
```bash
git commit -m "Mensagem"
```
- Para commitar também os arquivos versionados mesmo não estando no Stage basta adicionar o parâmetro `-a`:
```bash
git commit -a -m "Mensagem"
```

- Refazer commit quando esquecer de adicionar um arquivo no Stage (Diretório de Trabalho, Repositório):
```bash
git commit -m "Mensagem" --amend
```
> O **amend** é destrutivo e só deve ser utilizado antes do commit ter sido enviado ao servidor remoto.

# Como Reverter Alterações
Em qualquer fase do projeto, você pode querer desfazer alguma coisa. Veremos algumas ferramentas básicas para desfazer modificações que você fez. 
**Cuidado**, porque você pode desfazer algumas dessas mudanças. Esta é uma das raras situações no Git onde um deslize pode causar a perda definitiva de código.

- Para apagar o último histórico e resetar tudo:
```bash
git reset --hard HEAD~1
```

- Para desfazer o último commit, mas manter as alterações salvas no Stage:
```bash
git reset --soft HEAD~1
```

- Para forçar o projeto a voltar ao estado de um commit específico (via Hash):
```bash
git reset --hard XXXXXXXXXXX
```

# Recuperando commit apagado pelo git reset
Para visualizar os hashs:
```bash
git reflog
```

e para aplicar:
```bash
git merge <hash>
```
# Removendo Arquivos
> Apagar arquivos no fluxo do Git exige um pouquinho de atenção. Para sumir com um arquivo do seu repositório, você precisa tirá-lo da área de seleção (_stage_) e commitar a mudança. O comando `git rm` facilita isso, deletando o arquivo do Git e do seu diretório local ao mesmo tempo.

- Força a exclusão do arquivo no Git e no seu computador:
```bash
git rm -f <arquivo>
```

- Desfaz o monitoramento do arquivo, ou seja, o Git deixa de segui-lo, mas o arquivo físico continua intacto na sua máquina.
```bash
git rm --cached + <arquivo>
```
- Comando terminal direto (fora do Git) para apagar uma pasta inteira instantaneamente.
```bash
`rm -rf <arquivo>`
```

> Nota de Segurança: Se você alterou um arquivo e já o adicionou ao _stage_, o Git vai bloquear a remoção comum para proteger seu trabalho. Para prosseguir mesmo assim, você deve forçar a barra usando o argumento `-f`. Como esses dados ainda não estão em um _snapshot_ (commit), eles não poderão ser recuperados depois.

# Movendo e renomeando arquivos

Diferentemente de muitos sistemas de controle de versão (VCS), o Git não monitora explicitamente arquivos movidos ou renomeados.

Apesar disso, o Git possui o comando `git mv`, que permite mover ou renomear arquivos de forma prática.

## Sintaxe

```bash
git mv arquivo_origem arquivo_destino
```

### Exemplo

```bash
git mv README.txt README.md
```

**Finalidade:** O comando `git mv` move ou renomeia um arquivo e prepara automaticamente essa alteração para o próximo commit.

Após executar o comando, você pode verificar a alteração utilizando:

```bash
git status
```

O Git identificará que o arquivo foi renomeado.

---

## Como o `git mv` funciona?

Internamente, o comando `git mv` equivale à execução dos seguintes comandos:

```bash
mv README.txt README.md
git rm README.txt
git add README.md
```

O Git identifica automaticamente que se trata de um renomeamento. Portanto, você pode renomear o arquivo manualmente utilizando o explorador de arquivos ou o terminal e, em seguida, executar os comandos `git rm` e `git add` antes de criar um commit.

A principal vantagem do `git mv` é a praticidade, pois ele executa essas etapas em um único comando.

## Fazendo Stash
Muitas vezes, quando você está trabalhando em uma parte do seu projeto, as coisas estão em um estado confuso e você quer mudar de branch por um tempo para trabalhar em outra coisa. O problema é, você não quer fazer o commit de um trabalho incompleto somente para voltar a ele mais tarde. A resposta para esse problema é o comando `git stash`.

Você quer mudar de branch, mas não quer fazer o commit do que você ainda está trabalhando; você irá fazer o stash das modificações. Para fazer um novo stash na sua pilha, execute:
```bash
git stash
```
> Seu diretório de trabalho estará limpo. Neste momento, você pode facilmente mudar de branch e trabalhar em outra coisa; suas alterações estão armazenadas na sua pilha.

- Para ver stashes que você guardou, você pode usar:
```bash
git stash list
```
Você pode aplicar aquele que acabou de fazer o stash com o comando mostrado na saída de ajuda do comando stash original:

```bash
git stash apply
```
> Se você quer aplicar um dos stashes mais antigos, você pode especifica-lo, assim:  `git stash apply stash@{2}`. 
Se você não especificar um stash, Git assume que é o stash mais recente e tenta aplicá-lo.

## Tag
O Git tem a habilidade de criar tags em pontos específicos na história do código como pontos importantes. Geralmente as pessoas usam esta funcionalidade para marcar pontos de release (v1.0, e por ai vai). Nesta seção, mostraremos como listar as tags disponíveis, como criar novas tags, e quais são os tipos diferentes de tags.

- Para listar as `tags` execute:
```bash
git tag
```
- Para criar uma`tag` basta executar o seguinte comando, caso não queira criar a `tag anotada`, somente retire os parâmetro `-a` e `-m`.
```bash
git tag -a v1.4 -m 'my version 1.4'`.
```
# Compartilhar e Atualizar Projetos

#### Fazendo o Fetch
- Para pegar dados dos seus projetos remotos, você pode executar:
```bash
git fetch origin
```
Esse comando vai até o projeto remoto e pega todos os dados que você ainda não tem. Depois de fazer isso, você deve ter referencias para todos os branches desse remoto, onde você pode fazer o merge ou inspecionar a qualquer momento.

## Atualizando local
Incorpora as alterações de um repositório remoto no branch atual. Em seu modo padrão, `git pull` é uma abreviação para `git fetch` seguindo de git merge `FETCH_HEAD`. Por exemplo, se eu estiver em uma branch chamada `develop` e quiser atualizar caso haja atualizações remotamente:
```bash
`git pull origin develop`
```
## Empurrando seus commits
```bash
git push
``` 
> é o comando em que você transfere commits a partir do seu repositório local para um repositório remoto. É a contrapartida do `git fetch`, que busca importações e comprometem as agencias locais, utilizando o `git push` as exportações comprometem as filiais remotas.

Para fazer isso, você executa o `git push <nome_do_repositorio><nome_da_sua_branch-_local>`, que vai tentar fazer que `<nome_do_repositorio_remoto>` receba a sua branch `<nome_da_sua_branch_local>` contendo todos seus commits com alterações. 

Por exemplo:
```bash
git push origin develop
```

# Repositórios Remotos
Para ver quais servidores remotos você configurou, execute o comando `git remote`. Ele lista os nomes abreviados de cada repositório remoto que você configurou. 

- Para ver as URLs que o Git armazenou para leitura e escrita, adiciona `-v`:
```bash
git remote -v
```
- Para adicionar um novo repositório remoto com um nome abreviado que você pode referências facilmente:
```bash
git remo add <apelido> <URL>
```
- Para remover uma referencia de repositório remoto:
```bash
git remote remove <nome>`
```
- Para ver informações destalhadas sobre um repositório remoto específico:
```bash
git remote show <nome>
```
# Submódulos
> Os submódulos permitem que você inclua um repositório Git como um subdiretório de outro repositório Git. Isso é útil quando você precisa incorporar bibliotecas externas ou projetos separados dentro do seu projeto principal.

- Para adicionar um submódulo ao seu projeto:
```bash
git submodule add <URL> <caminho>`
```
- Ao clonar um repositório que contém submódulos, você precisa inicializá-los e atualizá-los:
```bash
git submodule init
git submodule update
```
Ou você pode clonar recursivamente, o que faz tudo em um só passo:
```bash
git clone --recurse-submodule <URL>
```
- Para atualizar todos os submódulos para as ultimas versões remotas:
```bash
git submodule update --remote
```

# Exibindo Objetos
O comando `git show` exibe informações sobre objetos do Git (commits, tags, árvores, blobs). 

- Para ver os detalhes de um commit específico, incluindo o diff das alterações:
```bash
git show <hash_do_commit>
```
- Para ver o conteúdo de um arquivo em um commit específico:
```bash
git show <hash>:<caminho/do/arquivo>`
```
- Para exibir as informações de uma tag anotada:
```bash
git show v1.0
```
- Sem argumentos, exibe os detalhes do último commit:
```bash
git show`
```

## Desafio: Desfazer um commit sem apagar o histórico

## Cenário

Pedro realizou um commit e enviou para o GitHub. Após alguns testes, percebeu que a alteração causou erros no sistema. Como outros membros da equipe já baixaram esse commit, ele não quer apagar o histórico do repositório.

## Solução: git revert

O comando `git revert` cria um novo commit que desfaz as alterações de um commit anterior, mantendo o histórico do projeto intacto.

## Passo a passo

1. Verificar o histórico de commits

```bash
git log --oneline
``` 

Exemplo de saída: 

a1b2c3d Adiciona tela de login 

e4f5g6h Corrige erro no cadastro

2. Reverter o commit problemático
```bash 
git revert a1b2c3d
```
O git criará automaticamente um novo commit desfazendo as alterações.

3. Enviar a correção para o GitHub
```bash
git push origin main
```

## Resultado 

Utilizando o `git revert`, Pedro consegue desfazer um commit incorreto sem alterar o histórico do projeto, garantindo que todos os membros da equipe continuem sincronizados.

## Desafio 2: Aproveitar apenas um commit de outra branch

## Cenário

Pedro está trabalhando na branch `nova-feature`, onde realizou vários commits. Durante o desenvolvimento, percebe que um dos commits contém uma correção importante que também precisa estar na branch `main`.

No entanto, ele não quer mesclar toda a branch, apenas aquele commit específico.

## Solução: git cherry-pick

O comando `git cherry-pick` permite copiar um commit específico de uma branch para outra.

## Passo a passo

1. Visualizar o histórico da branch
```bash
git log --online
```

Exemplo:

a1b2c3d Corrige erro no login 

e4f5g6h Adiciona tela de cadastro

2. Trocar para a branch que receberá a correção
```bash
git checkout main
```

3. Aplicar apenas o commit desejado
```bash
git cherry-pick a1b2c3d
```

O git copiára apenas as alterações daquele commit para a branch atual.

4. Enviar a atualização para o repositório remoto
```bash
git push origin main
```

## Resultado

Utilizando `git cherry-pick`, Pedro consegue reaproveitar uma correção importante sem precisar mesclar toda a branch `nova-feature`, evitando alterações desnecessárias na `main`.
 <hr>

## Colaboradores
<a href="https://github.com/gavvdev" title="gavvdev">
  <img src="https://github.com/gavvdev.png?size=100" width="72" alt="gavvdev" />
</a>
&nbsp;&nbsp;&nbsp;
<a href="https://github.com/LucasEmmanoel06" title="LucasEmmanoel06">
  <img src="https://github.com/LucasEmmanoel06.png?size=100" width="72" alt="LucasEmmanoel06" />
</a>
&nbsp;&nbsp;&nbsp;
<a href="https://github.com/Mariana-ASM" title="Mariana-ASM">
  <img src="https://github.com/Mariana-ASM.png?size=100" width="72" alt="Mariana-ASM" />
</a>
&nbsp;&nbsp;&nbsp;
<a href="https://github.com/PedroDelmiro13" title="PedroDelmiro13">
  <img src="https://github.com/PedroDelmiro13.png?size=100" width="72" alt="PedroDelmiro13" />
</a>
&nbsp;&nbsp;&nbsp;
<a href="https://github.com/VitorJunior60" title="VitorJunior60">
  <img src="https://github.com/VitorJunior60.png?size=100" width="72" alt="VitorJunior60" />
</a>
