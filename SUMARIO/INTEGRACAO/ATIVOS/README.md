# 🪪Ativos

##### Ativos [GET]

> [GET] https://wayds.net:8081/integraway/api/v1/ativo/

Esse endpoint retorna **TODOS** os ativos.
___
##### Resumo dos Ativos [GET]

> [GET] https://wayds.net:8081/integraway/api/v1/ativo/resumo

Esse endpoint retorna nome do estabelecimento e seu respectivo código.
___
##### Temperatura dos Ativos [GET]

> [GET] https://wayds.net:8081/integraway/api/v1/ativo/temperatura?codigoSensor=1234&data=2024-01-01&incluirCoordenadas=true

Esse endpoint retorna a temperatura e a data, baseadas no código do sensor do ativo.

Os parâmetros de codigoSensor e data são obrigatórios para que os dados do ativo possam ser retornados.

O parâmetro incluirCoordenas é opcional, este por sua vez retorna as coordenadas do local em que aquele ativo esteve presente, mediante data marcada, porém é necessário passar o valor **true** para esse parâmetro para que as coordenadas possam ser devolvidas para visualização do usuário.
___
##### Umidade dos Ativos [GET]

> [GET] https://wayds.net:8081/integraway/api/v1/ativo/umidade?codigoSensor=1234&data=2024-01-01

Esse endpoint retorna a umidade e a data, baseadas no código do sensor do ativo.
___
### **Coordenadas dos Ativos [GET]**

> [GET] https://wayds.net:8081/integraway/api/v1/ativo/umidade?codigoSensor=1234&data=2024-01-01

Esse endpoint retorna as coordenadas e a data, baseadas no código do sensor do ativo.