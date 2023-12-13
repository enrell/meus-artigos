## O que é GitHub?

O [GitHub](https://github.com) é uma plataforma de desenvolvimento baseado em Git, lá você encontra uma gama de ferramentas úteis para o desenvolvimento de qualquer tipo de aplicação, para pessoas e empresas.

O GitHub não é a única plataforma desse tipo, existem diversas plataformas que oferecem essas ferramentas. Sites que oferecem ferramentas semelhantes: SourceForge, Bitbucket, GitLab (não é da Microsoft e não é um complemento ao GitHub) e GNU Savannah (destinado a projetos de software livre).

#### Ferramentas

Uma das principais ferramentas é o sistema de armazenamento, os repositórios ou (Repositories), eles são responsáveis por guardar sua aplicação de forma segura e distribuída, Algumas das principais características e funcionalidades do GitHub incluem:

- Controle de Versão Distribuído: O GitHub utiliza o Git, um sistema de controle de versão distribuído que permite que várias pessoas trabalhem em um projeto simultaneamente, sem interferir no trabalho um do outro. 
- **Colaboração:** O GitHub facilita a colaboração entre desenvolvedores. Vários desenvolvedores podem contribuir para um projeto, propor alterações (pull requests), relatar problemas (issues) e discutir questões relacionadas ao desenvolvimento.
- **Rastreamento de Problemas:** Os problemas (issues) são usados para rastrear tarefas, bugs, melhorias e outras discussões relacionadas ao projeto. Isso ajuda a organizar o trabalho e facilita a comunicação entre os membros da equipe.
- **Pull Requests:** Os pull requests são usados para propor e discutir alterações no código-fonte. Eles permitem que os desenvolvedores revisem as alterações feitas por outros antes de serem mescladas no projeto principal.
- **Integração Contínua:** O GitHub suporta integração contínua, o que significa que os desenvolvedores podem configurar pipelines (conjunto de processos e ferramentas automatizados) para testar e construir seu código sempre que uma alteração é proposta.
- **GitHub Actions:** Uma funcionalidade que permite a automação de fluxos de trabalho, como testes, compilação e implantação diretamente no GitHub.
- **Licenciamento:** Os repositórios do GitHub muitas vezes incluem informações sobre a licença do software, ajudando a definir como o código pode ser usado por outras pessoas. Você pode definir uma licença através do arquivo LICENSE.

#### É seguro?

- Chaves SSH: O GitHub usa chaves SSH para autenticação. As chaves SSH são pares de chave pública e privada, e o GitHub autentica você com base na chave pública associada à sua conta.

-  Controle de Acesso: O GitHub permite que você configure permissões de acesso para seus repositórios. Você pode controlar quem pode visualizar, clonar, enviar alterações ou administrar um repositório. Isso ajuda a garantir que apenas pessoas autorizadas possam interagir com o código.

- Autenticação em Dois Fatores (2FA): O GitHub suporta autenticação em dois fatores, que adiciona uma camada adicional de segurança ao exigir uma segunda forma de autenticação além da senha.

- Políticas de Segurança: O GitHub implementa práticas de segurança e monitora constantemente a atividade para identificar e responder a potenciais ameaças.

- Backup: O GitHub realiza backups regulares dos dados para evitar perdas de dados em caso de falhas nos servidores.

## Como criar um repositório no GitHub?

A forma mais indicada para a criar um repositório no GitHub é através do próprio site do GitHub:

![[print-criar-repo-1.png]]
![[print-criar-repo-2.png]]

1. **Nome do Repositório:** Escolha um nome usando apenas letras, números, `.`, `-` ou `_`.
2. **Descrição (Opcional):** Adicione uma descrição ao seu projeto.
3. **README:** Marque a opção para incluir um README, um arquivo de texto que descreve seu projeto.
4. **Importação de Projeto Existente:** Se já tem um projeto, crie o repositório com README para facilitar. Depois, clone para seu computador, copie os arquivos do projeto para a pasta do repositório e faça o "push" para o GitHub.

![[prit-criar-repo-3.png]]

#### Criei um repositório de exemplo

![[print-criar-repo-4.png]]

![[print-criar-repo-5.png]]

## Importando um projeto e subindo para o GitHub

O primeiro passo é criar um par de chaves SSH,