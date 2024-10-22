# Entendendo sobre Segurança e Identidade na Azure

## Entra ID
 * É o antigo Active Directory, gerencia os usuários.
 * Permite sincronizar os usuários no ambiente OnPremisse com Azure.
 * Usuários criazos no Azure não são sincronizados em On Premisse. Apenas usuários On Premisse são sincronizados.

### Usuários

 * Ao Excluir um usuário, é possível restaurá-lo em até 30 dias depois de ser deletado.
 * É possível configurar o Self-Service Password Reset;
 * É possível criar um novo usuário ou convidar um usuário externo;
 * Os usuários podem ser personalizados com o domínimo da empresa;
 * É possível realizar a criação, convite e exclusão de diversos usuários simultaneamente;

### Roles and Administrators
Tem relação com o permissionamento com relação as outras contas, mas não tem permissionamento com relação a criação/exclusão de recursos.

### Microsoft Entra Connect

Através dele é possível realizar uma conexão onde é replicado os usuários do ambiente On Premisse para o ambiente de Nuvem (Azure);

### Custom domain names

Onde a organização vai utilizar os domínios da empresa, depois de serem verificados.

### Health 

Mostra como esta o SLA (Disponibilidade do serviço)

### Persionamentos
Ele é atribuído diretamente no recurso, podendo assim cada recurso gerenciar seus próprios permissionamentos, através da opção Access control (IAM)

Como o permissionamento é herdável, pode ser configurado em um Resource Group e desta forma herdado por todos os recursos que fizerem parte dele.

## Microsoft Defender for Cloud

 * É um termômetro que mostra uma analise de postura de segurança, mostrando nosso nível atual (quão bom ou ruim estamos).
 * Ela é uma aplicação nativa de nuvem.
 * Ele é hibrido e multinuvem.
 * Fornece recomendações de segurança;
 * Possui uma nota para nível de segurança;
 * Pode ser conectado a conta DevOps, GitHub, Git Labs, e vai validar os códigos que subirem e forem executados na nuvem.
 * Permite configuração de Alertas para serem enviados ao email, Teams, Slack, etc.
 
 