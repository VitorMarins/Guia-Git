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

# Tipos de controle de versão

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
 
# Comandos Git 

Os comandos Git são utilizados para controlar as versões de projetos, registrar alterações e facilitar o trabalho em equipe. A seguir estão os principais comandos utilizados no dia a dia de um desenvolvedor. 
`git config` - Configura informações do usuário que serão associadas aos commits.
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@email.com"
git config --local user.name "Seu Nome"
git config --local user.email "seuemail@email.com"
```
`git init` - Inicializa um novo repositório Git na pasta atual. 
```bash
git init
```
`git clone` - Cria uma cópia local de um repositório remoto. 

```bash
git clone https://github.com/usuario/repositorio.git
```
`git status` - Exibe o estado atual do repositório, mostrando arquivos modificados, adicionados e não rastreados. 
```bash
git status
```
`git add` - Adiciona arquivos para a área de preparação (staging area).
```bash
git add arquivo.txt (Adicionar um arquivo)
git add . (Adicionar todos os arquivos alterados)
```
`git commit` - Registra as alterações adicionadas ao histórico do projeto. 
```bash
git commit -m "Adiciona tela de login"
```
`git log` - Mostra o histórico de commits do repositório. 
```bash
git log
git log --oneline (Versão resumida)
```
`git diff` - Mostra as diferenças entre versões de arquivos. 

```bash
git diff
```
`git branch` - Lista, cria ou remove branches.
```bash
git branch (Listar branches)
git branch nova-feature (Criar uma branch)
git branch -d nova-feature (Deleta uma branch)
```
`git checkout` - Permite trocar de branch. 
```bash
git checkout nova-feature
git checkout -b nova-feature (Cria e muda para a branch criada)
```
`git switch` - Alternativa moderna para trocar de branch. 
```bash
git switch nova-feature
```
`git merge` - Mescla alterações de uma branch com outra. 
```bash
git merge nova-feature
```
`git remote add origin` - Conecta o repositório local a um repositório remoto. 
```bash
git remote add origin https://github.com/usuario/repositorio.git
```
`git push` - Envia commits locais para o repositório remoto. 
```bash
git push origin main
```
`git pull` - Baixa e integra alterações do repositório remoto. 
```bash
git pull origin main
```
`git fetch` - Baixa alterações do repositório remoto sem aplicá-las automaticamente. 
```bash
git fetch
```
`git reset` - Remove arquivos da área de preparação ou retorna o projeto para um estado anterior. 
```bash
git reset HEAD arquivo.txt
```
`git restore` - Descarta alterações realizadas em arquivos. 
```bash
git restore arquivo.txt
```

 <hr>
<br>

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
