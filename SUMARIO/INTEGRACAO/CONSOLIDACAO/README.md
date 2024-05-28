# ⚙️Consolidação

Após a montagem da roteirização e faturamento dos pedidos existe a etapa de**Consolidação**, onde a empresa verifica se os pedidos e itens faturados batem com os listados na roteirização. Em caso de discrepância, é realizada uma alteração nos respectivos pedidos visando a conformidade entre os pedidos **faturados** e **roteirizados**.

Seguem os endpoints serão utilizados para realizar a consolidação:

##### Atualizar pedidos [PATCH]

> [PATCH] https://wayds.net:8081/integraway/api/v1/pedido/many

Para realizar a atualização dos pedidos, deve ser utilizado este endpoint. Nele deve ser enviado um Array de objetos do tipo "Entrega". Esse objeto é composto pelos atributos "codigo", que é o código da entrega, "codigoCliente", que é o código do cliente e "pedidos", que são os pedidos dessa entrega(olhar documentação no Swagger).
___
##### Deletar pedidos [DELETE]

> [DELETE] https://wayds.net:8081/integraway/api/v1/pedido

Para deletar vários pedidos utilizar esse endpoint(olhar documentação no Swagger).
___
##### Deletar pedido por Id [DELETE]

> [DELETE] https://wayds.net:8081/integraway/api/v1/pedido?codigopedido=12345

Para deletar apenas **UM** pedido utilizar esse endpoint informando seu **ID**.

* Parameters
    * codigopedido (Required, Number) - Código de identificação do pedido à ser deletado
    * codigoentrega (Optional, Long)- Código da entrega