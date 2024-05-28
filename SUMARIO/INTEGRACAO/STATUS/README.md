# ✅Status das Entregas

Após a consolidação final e certificação da conformidade das rotas, é possível buscar o status das entregas através do seguinte endpoint.

##### Rotas completas [GET]

> [GET] https://wayds.net:8081/integraway/api/v1/rota?codigorota=12345

Esse endpoint retornará a rota completa, onde é possivel encontrar suas entregas e com isso buscar o status dos seus pedidos.

* Parameters
    * codigoRota (Required, String) - Código da rota a ser buscada
    * dataInicial (Required, Date) - Período de ínicio para busca
    * dataFinal (Required, Date) - Período final para busca