## Disclaimer
Leia tudo de forma sequencial, é importante não pular etapas. Algumas partes do texto dão o contexto necessário para o entendimento.

## O que é Git?

No repositório do [Git](https://github.com/git/git) no GitHub os desenvolvedores do Git o definem como:
> "É um sistema de controle de revisão rápido, escalável e distribuído, com um conjunto de comandos excepcionalmente rico que oferece operações em níveis elevados e acesso completo às partes internas."

O Git é um projeto de código aberto coberto pela Licença Pública Geral GNU versão 2 (algumas partes estão sob licenças diferentes, compatíveis com a GPLv2). Foi originalmente escrito por Linus Torvalds criador do [Linux](https://github.com/torvalds/linux) com a ajuda de um grupo de hackers ao redor da internet.

## Por que usar Git?

Se você já se viu duplicando projetos e renomeando pastas para criar versões diferentes, sabe como isso pode complicar as coisas. Trabalhar assim em equipe aumenta os desafios.

O Git funciona como um histórico de alterações para o seu projeto. Em vez de modificar diretamente o projeto principal, você cria "ramificações" para experimentar ideias. Quando tudo estiver pronto, você "confirma" essas mudanças, criando um registro claro do que foi feito.

Isso não apenas mantém tudo organizado, mas também facilita a colaboração em equipe. Se outros estiverem trabalhando no projeto, o Git ajuda a juntar todas as mudanças de maneira tranquila.

Então, da próxima vez que pensar em fazer cópias e renomeações loucas, considere adotar o Git. Ele tornará seu projeto mais organizado, eficiente e colaborativo, sem aquela confusão toda. 

## Comandos básicos do Git

<mark>OBS:</mark> Alguns comandos deste tópico tem vantagens e desvantagens em serem usados, neste tópico não irei tratar delas, ficará para outro post.

- <code>git init</code>

O primeiro comando básico que você vai usar é o <code>git init</code>, mas o que ele faz? para que serve?

O <code>git init</code> é usado para iniciar um novo repositório Git em um diretório existente ou em um novo diretório vazio. Ao executar <code>git init</code>, você está basicamente informando ao Git para começar a rastrear as alterações nos arquivos dentro desse diretório.

Quando você executa <code>git init</code>, alguns arquivos e diretórios específicos são criados dentro do diretório do seu projeto. O principal deles é o diretório oculto chamado .git, que contém toda a estrutura necessária para o Git controlar as versões dos seus arquivos.

<mark>NÃO EXCLUA A PASTA .git DE FORMA ALGUMA!</mark>
Se você fizer isso, apagará todo seu histórico de modificações do seu repositório local.

- <code>git config user.name</code> e <code>git config user.email</code>

Os comandos <code>git config user.name</code> e <code>git config user.email</code> são usados para configurar o nome do usuário e o endereço de e-mail associados aos commits que você faz em um repositório Git. Essas informações são incluídas em cada commit para identificar quem fez as alterações. Esses comandos são um passo importante para a identificação da pessoa que fez o commit, fundamental para a comunicação da equipe. Você irá usar da seguinte forma: <code>git config user.name (seu nome aqui)</code>, não esqueça de remover os (), a mesma sintaxe vale para o email.

- <code>git add</code>

O comando <code>git add</code> é utilizado no Git para adicionar mudanças específicas em arquivos ao chamado "index" (ou "staging area") vou explicar esses termos mais tarde. Essa etapa é necessária antes de realizar um commit para registrar as alterações no histórico do repositório.

Quando você faz alterações em seus arquivos, o Git precisa saber quais dessas alterações você deseja incluir no próximo commit. O <code>git add</code> permite que você selecione as mudanças específicas que você quer incluir, preparando-as para o próximo commit. Você irá usar da seguinte maneira: <code>git add (nome do seu arquivo com sua extensão)</code>.

- <code>git add .</code>
O comando <code>git add .</code> é utilizado para adicionar todas as mudanças que você fez ao "staging" (ou "área de preparação"), ou seja, todas as mudanças feitas nos seus arquivos serão preparadas para o commit.

Eu recomendo cuidado ao usar o comando `<code>git add .</code>`, por exemplo:

Imagine que você tenha feito a página "sobre.html" do seu projeto e também feito algumas mudanças na página "home.html". No entanto, você só deseja fazer o commit das alterações na página "sobre" para manter as coisas organizadas.

Se você usar `<code>git add .</code>`, você estará adicionando as mudanças tanto da página "sobre.html" quanto da "home.html" para o próximo commit, o que pode não ser o que você quer. Para evitar esse problema, é melhor usar `<code>git add sobre.html</code>`. Em seguida, você pode fazer o commit para registrar apenas as alterações na página "sobre.html" e manter seu histórico de versões mais preciso e organizado.

## O que é Commit?

E finalmente, o tão citado commit, uma peça fundamental no uso do Git.

Em termos simples, um commit no Git representa uma captura instantânea do seu projeto em um determinado momento. É como tirar uma foto do estado atual dos seus arquivos, incluindo todas as alterações que você adicionou ao "staging area" (ou "área de preparação") com o comando `git add`.

Cada commit é associado a uma mensagem descritiva, que serve para explicar o propósito daquela alteração. Essas mensagens são cruciais para entender o histórico do seu projeto e facilitam a colaboração em equipe, já que outros desenvolvedores podem compreender suas mudanças apenas lendo as mensagens dos commits.

**Como usar `git commit -m "mensagem descritiva"`:**

Após usar `git add` para preparar as alterações, o próximo passo é usar `git commit` para criar um commit.

- **Sintaxe básica:**
  ```bash
  git commit -m "mensagem descritiva"
  ```
  
  - `-m`: Permite adicionar uma mensagem descritiva diretamente na linha de comando.

**Dicas para mensagens de commit:**

1. **Seja Descritivo:** A mensagem deve explicar o que a alteração realiza. Evite mensagens vagas como "correções" ou "mudanças".

2. **Seja Conciso:** Mantenha a mensagem curta e objetiva. Evite explicações excessivamente detalhadas.

3. **Use o Presente:** Mantenha a consistência no tempo verbal. Prefira o tempo presente, como em "Adiciona funcionalidade" em vez de "Adicionou funcionalidade".

Caso esteja disposto a aprender um padrão de commits recomendo o [Conventional Commits](https://www.conventionalcommits.org/pt-br).

## Próximos capítulos

Para o próximo capítulo vou mostrar como usar o git juntamente com o GitHub.
