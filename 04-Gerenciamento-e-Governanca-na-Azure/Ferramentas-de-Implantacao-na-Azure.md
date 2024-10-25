# Ferramentas de Implantação na Azure

## Azure PowerShell

É representado por um ícone com os símbulos ">_", e pode ser encontrado ao lado direito da barra de pesquisa.

Para conseguir utilizá-lo é necessário ter pelo menos um Storage Account.

Além da opção do PowerShell, pode se escolher a opção de utilizar o Bach para quem se sinta mais a vontade com seu uso.

Pode ser feito tanto upload quando download de arquivos através de botões de ferramenta quando ele é aberto.

## Automação

#### CLI/PS

Entre as opções dos recursos, temos uma área dedicada a Automação, entre eles o CLI/PS (PowerShell).

Quando acessamos o CL/PS, temos as opções de comandos para o recurso que esta sendo utilizado, além de informações uteis para entender como funciona.


#### Export template

A opção Export template permite que vejamos as informações necessárias para criação do recurso em que estamos.

Eles podem ser utilizados para automatizar as próximas criações dos recursos, além de estudos analisando suas linhas.

#### Bicep Playground 

O Bicep é uma linguagem específica de domínio (DSL) que usa sintaxe declarativa para implantar recursos do Azure. Em um arquivo Bicep, você define a infraestrutura que deseja implantar no Azure e, em seguida, usa esse arquivo durante todo o ciclo de vida de desenvolvimento para implantar repetidamente a sua infraestrutura. Os seus recursos são implantados de maneira consistente.

O Bicep fornece sintaxe concisa, segurança de tipos confiável e suporte para reutilização de código. O Bicep uma experiência de criação de alto nível para suas soluções de infraestrutura como código no Azure.

O Bicep facilita a criação dos recursos, simplicando a quantidade de dados necessários, quando comparado com o JSON do template.

Link: https://azure.github.io/bicep/

# Azure ARC
Ferramenta de Gerenciamento Multicloud.

Ele vem disponível em todas as assinaturas, mas deve ser configurado para ser utilizado.

Ele permite que recursos fora do Azure sejam administrados na Azure, e também que recursos do Azure sejam gerenciados fora do Azure, facilitando a gestão e centralização dos recursos.

