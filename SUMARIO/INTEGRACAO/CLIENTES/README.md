# 👨‍💻Integração de Clientes

A integração de Cliente é feita cliente a cliente, por meio dos seguintes endpoits:

##### Inserir clientes [PUT]

> [PUT] https://wayds.net:8081/integraway/api/v1/cliente

Esse endpoint tem a função de importar clientes do **ERP para a Plataforma da Way Data**.

Para seu funcionamento, é necessário o envio de um cliente no JSON/Body, que deve seguir o padrão da Way Data, exemplificado abaixo:

![](/assets/put_cliente_json.png)

___
##### Atualizar cliente [PATCH]

> [PATCH] https://wayds.net:8081/integraway/api/v1/cliente

Caso seja necessário atualizar um cliente (recomendado apenas em casos de mudanças de endereço) é utilizado este endpoint.

* Parameters
    * codigoAntigo (string, optional) - Código do cliente que será atualizado
    * apenasBuscaPrecisa (boolean, optional) - Mecanismo para busca de endereço de maneira precisa (as informações de endereço precisam estar corretas)

___
##### Buscar clientes [GET]

> [GET] https://wayds.net:8081/integraway/api/v1/cliente?pagina=1&quantidade=100

Para buscar os clientes já cadastradors na plataforma da WayData, é feita uma chamada nesse endpoint.

Nessa requisição, o resultado vem por padrão paginado. Ou seja, caso seja necessário recuperar todos os clientes em uma única chamada, você deve passar os **Query Parameters** **"pagina"** e **"quantidade"** junto da requisição, semelhante ao exemplo acima. Caso seja necessário filtrar clientes de uma forma mais granular, recomendamos que a documentação da api seja consultada para encontrar o filtro que mais se adequa a requisição desejada.

* Parameters
    * pagina (required, number) - Página de busca
    * quantidade (required, number) - Quantidade de itens por página
    * uf (optional, string) - Unidade federativa
    * municipio (optional, string) - Município de origem
    * classificacao (optional, string) - Tag do cliente
___
##### Recuperar clientes por Id [GET]

> [GET] https://wayds.net:8081/integraway/api/v1/cliente/id?codigo=12345

Por fim, um exemplo, essencial para fim de testes, é a busca de um único cliente, por meio do seu código, informado na hora do cadastro.

* Parameters
    * codigo (required, number) - Codigo informnado na hora do cadastro
    * apenasAtivos (optional, boolean) - Flag para buscar apenas clientes ativos

<br>
<br>
**Observações**:
A plataforma da WayData transforma endereços por extenso em coordenadas. Dessa forma, existe uma ordem de prioridade Coordenadas > Endereço. Nesse sentido, caso sejam
enviadas Coordenadas, qualquer outra informação de endereço é ignorada.
Caso não possua Coordenadas, você não deve passar essas informações no corpo da requisição, sendo necessário somente o endereço.