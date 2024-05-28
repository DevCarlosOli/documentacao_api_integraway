# 📦Integração de Remessas:

A importação dos pedidos para a Way Data é feita pelos endpoints de **REMESSA**. É importante ressaltar, que diversas remessas podem ser cadastradas simultaneamente.

Como mostrado no **RESUMO** da integração, um pedido quando é importado para Way Data tem **DOIS** estados **INDEPENDENTES**. O estado inicial, no momento que o pedido é importado, é quando esse novo pedido ainda não está associado a nenhuma **ROTEIRIZAÇÃO**, sendo assim, nesse momento chamado de **REMESSA**. Segue então que, o ciclo de vida de uma REMESSA começa quando ela é importada para a plataforma da Way Data e termina quando ela é importada para uma **ROTEIRIZAÇÃO**. A partir do momento em que uma remessa é associada à uma roteirização, inicia-se um novo ciclo no qual ela efetivamente é um **PEDIDO**.

Para integração das remessas são utilizados os seguintes endpoints:

##### Inserir remessas [PUT]

> [PUT] https://wayds.net:8081/integraway/api/v1/remessa/many

Este endpoint é utilizado para inserir remessas. Para seu funcionamento, é necessário que os dados enviados JSON/Body sejam um Array de objetos do tipo remessa, que está de acordo com o formato da Way Data.
Segue Exemplo:

![](/assets/put_remessa_json.png)

___
##### Buscar remessas [GET]

> [GET] https://wayds.net:8081/integraway/api/v1/remessa

Para buscar uma remessa, este seria o endpoint apropriado. É opcional enviar os seguintes parametros:

* Parameters
    * numeroRemessa (optional, string) - Codigo da remessa
    * flagNaoRoteirizado (optional, boolean) - Flag para mostrar apenas as remessas que não entraram em rota e ou mostrar as que estão em rota e também não estão
___
##### Deletar remessas [DELETE]

> [DELETE] https://wayds.net:8081/integraway/api/v1/remessa

Para deletar uma remessa, este seria o endpoint apropriado. É necessário enviar um array no JSON/Body da requisição com os códigos das remessas que devem ser apagadas.
___
##### Atualizar remessas [PATCH]

> [PATCH] https://wayds.net:8081/integraway/api/v1/remessa/many

Para realizar a atualização de uma remessa você deve utilizar este endpoint e partir do mesmo princípio da inserção, onde deve ser enviado um Array de objetos do tipo remessa no JSON/Body da requisição, com as remessas que devem ser alteradas.
