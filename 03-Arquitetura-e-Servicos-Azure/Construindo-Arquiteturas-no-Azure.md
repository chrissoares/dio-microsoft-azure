# Construindo Arquiteturas no Azure

Site para explorar a infraestrutura global do Azure: https://azure.microsoft.com/pt-br/explore/global-infrastructure/

Podemos ver o globo onde temos marcados as infrasestruturas do Azure espalhadas pelo planeta, com informações sobre cada uma delas.
Inclusive existem links para informações mais detalhadas sobre cada local/região.

Também é possível realizar um Tour Virtual por um Datacenter do Azure.
Mostrando assim o padrão que é adotado em todos os Datacenters do Azure quanto a segurança, qualidade do serviço, etc.

### Grupo de Recursos

Um grupo de recursos é um container que vc usa para gerenciar e agregar recursos em uma única unidade.

Os recursos podem existir em apenas um grupo de recursos.

Os recursos podem existir em diferentes regiões.

Os recursos podem ser movidos para diferentes grupos de recursos.

Os aplicativos podem utilizar vários grupos de recursos.

Possui marcações para ajudar a organizar por diferentes categorias.
A marca consiste em uma chave (seu nome) e um valor.
O nome não faz diferenciação entre letras maiúsculas e minúsculas, mas o valor faz esta diferenciação.

Isto vai facilitar na hora que for verificado na fatura, pois virá a marcação do recurso.

Podemos ver no Grupo de Recursos
 * Logs de atividade: quando algo foi criado, excluído, quem fez, etc;
 * Controle de acesso pelo IAM: Pode permissionar apenas a esse grupo;
 * Pode ser definidos bloqueios que vão sobrepor as permissões;
 * Visualizar os recursos deste grupo;

 Depois do Grupo de Recurso criado, é possível adicionar os recursos criados a ele, como VNet,

 
