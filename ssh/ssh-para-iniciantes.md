## O que é SSH?

Descrito no documento oficial do [SSH](https://datatracker.ietf.org/doc/html/rfc4253) como:

>" The Secure Shell (SSH) Protocol is a protocol for secure remote login
   and other secure network services over an insecure network."

> "O Protocolo Secure Shell (SSH) é um protocolo para login remoto seguro e outros serviços de rede seguros sobre uma rede não segura."

Resumindo, é um protocolo de rede criptografado usado para comunicações seguras em uma rede não segura. Ele permite que usuários acessem e controlem remotamente dispositivos e servidores pela internet de forma segura.

O SSH fornece uma maneira segura de autenticar e trocar dados criptografados entre dois sistemas, prevenindo potenciais ameaças de interceptação ou manipulação de dados durante a transmissão. Isso é particularmente crucial ao acessar servidores remotos ou realizar tarefas administrativas em sistemas distribuídos.

Como SSH é um protocolo de rede, não uma ferramenta, temos que baixar uma ferramenta que nos disponha dos recursos necessários para usar o SSH.

No nosso caso vamos usar a "suite" (conjunto de ferramentas) [OpenSSH](https://www.openssh.com/), que é uma implementação de código aberto do protocolo SSH, em conjunto com ferramentas essenciais para nós desenvolvedores, todo desenvolvedor deve estudar SSH e Criptografia, é indispensável.

Vamos começar criando um par de chaves SSH com a ferramenta "ssh-keygen".

Para criar um par de chaves SSH usando um algoritmo moderno e rápido como o "ed25519" só precisamos passar o parâmetro "-t" para o gerador, e ele lhe guiará para a criação do par de chaves `ssh-keygen -t ed25519`.

### Mas o que é esse tal de "ed25519"?

O "ed25519" é um sistema de chaves públicas de curvas elípticas de utilizado para criptografia assimétrica, onde um par de chaves é gerado: uma chave privada e uma chave pública. Ele faz parte de uma família de curvas elípticas chamada "Curve25519", desenvolvida pelo renomado matemático Daniel J. Bernstein no ano de 2011. O algoritmo "ed25519" oferece vantagens significativas de segurança e desempenho sobre algoritmos mais antigos como o RSA e SHA-256.

## Chaves assimétricas

Chaves assimétricas, também conhecidas como criptografia de chave pública, são um tipo de sistema de criptografia que utiliza um par de chaves relacionadas, composto por uma chave pública e uma chave privada. Essas chaves são matematicamente relacionadas, mas as informações codificadas com uma chave só podem ser decodificadas pela outra chave do par. Isso significa que o que é criptografado com a chave pública só pode ser descriptografado pela chave privada correspondente, e vice-versa.

- **Chave Pública:** Essa chave é geralmente distribuída livremente e conhecida por todos. Ela é usada para criptografar informações que só podem ser decodificadas pela chave privada correspondente.

- **Chave Privada:** Esta chave é mantida em segredo e protegida pelo proprietário. É usada para descriptografar as informações que foram criptografadas com a chave pública correspondente.

O uso de chaves assimétricas é fundamental em vários aspectos da segurança digital, como autenticação, assinaturas digitais e troca segura de chaves de sessão em protocolos como o SSH (Secure Shell) e o SSL/TLS (usado para comunicação segura na web).

Um exemplo comum de aplicação é quando você acessa um site seguro (usando HTTPS). O servidor web possui uma chave privada que corresponde a uma chave pública incorporada no certificado SSL. Quando você envia informações para o servidor, a conexão é criptografada usando a chave pública no certificado, e apenas o servidor, com a chave privada correspondente, pode descriptografar essas informações. Isso garante a confidencialidade e a integridade dos dados transmitidos.

## Conclusão

Em conclusão, o SSH desempenha um papel fundamental na garantia da segurança das comunicações em redes, especialmente quando se trata de acesso remoto a dispositivos e servidores. Ao utilizar o protocolo SSH e implementar chaves assimétricas, como o algoritmo "ed25519", os desenvolvedores podem estabelecer conexões seguras, prevenindo ameaças de interceptação ou manipulação de dados durante a transmissão.

A escolha do algoritmo "ed25519" destaca a importância de algoritmos modernos e eficientes em comparação com métodos mais antigos. As chaves assimétricas desempenham um papel crucial na criptografia de chave pública, possibilitando autenticação segura, assinaturas digitais e a troca segura de informações em diversas aplicações, incluindo protocolos como SSH e SSL/TLS.

No contexto do desenvolvimento, a utilização da suite OpenSSH e a compreensão dos princípios de criptografia, incluindo chaves assimétricas, são consideradas indispensáveis. A criação de pares de chaves SSH, como exemplificado com o comando "ssh-keygen -t ed25519", demonstra um passo inicial essencial para garantir a segurança nas comunicações e acessos remotos.

Em resumo, o SSH e as chaves assimétricas desempenham um papel crucial na construção de um ambiente de desenvolvimento seguro, protegendo a integridade e confidencialidade das informações transmitidas pela rede. O conhecimento e a aplicação adequada desses conceitos são essenciais para qualquer desenvolvedor comprometido com a segurança de seus sistemas e comunicações.