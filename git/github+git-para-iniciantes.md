## O que é GitHub?

O [GitHub](https://github.com) é uma plataforma de desenvolvimento baseado em Git, lá você encontra uma gama de ferramentas úteis para o desenvolvimento de qualquer tipo de aplicação, para pessoas e empresas.

O GitHub não é a única plataforma desse tipo, existem diversas plataformas que oferecem essas ferramentas. Sites que oferecem ferramentas semelhantes: SourceForge, Bitbucket, GitLab (não é da Microsoft e não é um complemento ao GitHub) e GNU Savannah (destinado a projetos de software livre).

#### Ferramentas

Uma das principais ferramentas é o sistema de armazenamento, os repositórios ou (Repositories), eles são responsáveis por guardar sua aplicação de forma segura e distribuída, Algumas das principais características e funcionalidades do GitHub incluem:

- **Controle de Versão Distribuído**: O GitHub utiliza o Git, um sistema de controle de versão distribuído que permite que várias pessoas trabalhem em um projeto simultaneamente, sem interferir no trabalho um do outro. 
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

![[print-criar-repo-3.png]]

#### Criei um repositório de exemplo

![[print-criar-repo-4.png]]

![[print-criar-repo-5.png]]

## Importando um projeto e subindo para o GitHub

O primeiro passo é criar um par de chaves, leia o capitulo [[ssh-para-iniciantes]] para entender melhor.

1. Começamos gerando um par de chaves SSH utilizando o algoritmo "ed25519" de preferência.
```
ssh-keygen -t ed25519
```
2. A ferramenta vai lhe perguntar onde você quer guardar essa chave no seu sistema, recomendo que deixe no caminho padrão da seu sistema, você pode definir o nome da sua chave colocando o caminho padrão e substituindo o id_ed25519 pelo nome da sua chave, como por exemplo "github-key", essa vai ser sua chave privada, você não deve compartilhar ela com ninguém.
3. No próximo passo, defina uma senha para sua chave privada, toda vez que você for usar-la terá que colocar a sua respectiva senha, tenha sempre certeza de que não irá esquecer a sua senha, recomendo o uso de um gerenciador de senhas como o (Bitwarden).
4. No próximo passo, a ferramenta vai criar automaticamente a chave pública no mesmo diretório que você definiu inicialmente.
5. Depois vai imprimir no seu terminal um fingerprint, o fingerprint de uma chave SSH é uma representação única e curta da chave. É uma sequência de caracteres que serve como uma espécie de "impressão digital" da chave. O fingerprint é usado para verificar a autenticidade da chave e garantir que ela não tenha sido alterada. É comumente usada na primeira conexão com um servidor remoto, para evitar ataques ([man-in-the-middle](https://www.kaspersky.com.br/blog/what-is-a-man-in-the-middle-attack/462/)). Estamos apenas criando uma chave no seu computador local, portanto essa preocupação pode ser ignorada, existem outras ameaças mais graves, como [malwares](https://www.kaspersky.com.br/resource-center/preemptive-safety/what-is-malware-and-how-to-protect-against-it) ou [ransomwares](https://www.kaspersky.com.br/resource-center/threats/ransomware).
7. Você deve copiar todo o texto da chave pública que tem a extensão ".pub" para colar na sessão de SSH do GitHub.

Segue o caminho:

![[print-adicionar-ssh-1.png]]
![[print-adicionar-ssh-2.png]]
![[print-adicionar-ssh-3.png]]
![[print-adicionar-ssh-4.png]]

Nessa ultima etapa você deve definir um nome para a nova chave SSH, e colar a chave pública para o campo correspondente.

E pronto! você adicionou uma nova forma de autenticação no GitHub, agora você pode clonar os seus repositórios usando o clone via SSH:

![[print-adicionar-ssh-5.png]]

Dessa forma, você poderá usar o Git para enviar seus commit's de forma segura para seu repositório remoto no GitHub!

## Próximos capítulos

Para o próximo capítulo, vamos mergulhar na pura teoria do Git, e vamos resumir o controle de versão que conhecemos nos dias atuais.