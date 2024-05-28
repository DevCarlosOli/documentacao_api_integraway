# 🚚Roteirização:

Uma vez que os clientes e remessas ( nessa ordem ) foram integrados dentro da plataforma da Way Data, o Roteirista (ou o time de desenvolvimento do cliente que está fazendo a integração) tem insumos suficientes para gerar uma **ROTEIRIZAÇÃO** e criar **ROTAS** individuais para cada
veículo cadastrado.

A plataforma para acesso e criação das rotas, em ambiente de teste é: **https://wayds.net:8081/**

Os dados para acesso devem ser solicitados ao time de Sucesso do Cliente ou ao time de
integração.

Caso os desenvolvedores do time de integração do cliente tenham dúvidas sobre o uso da
plataforma, também é possível agendar treinamentos de uso da plataforma com o time do
Sucesso do Cliente.

### Passo a passo para realizar uma roteirização

* Clique na aba menu no canto inferior direito da página

![road1](https://user-images.githubusercontent.com/56355682/232779536-da00a15e-d6b1-4d18-a282-df9778efc685.png)

* Clique na opção RoadWay para abrir a guia referente à plataforma

![road2](https://user-images.githubusercontent.com/56355682/232779529-82ce868a-b2e2-497b-b5ab-e85bab5eb788.png)

* Na aba do RoadWay abra o menu

![road3](https://user-images.githubusercontent.com/56355682/232779520-55b65e81-0671-4723-af49-8a0108097c00.png)

* Selecione a opção "Novo" para criar uma nova roteirização

![road4](https://user-images.githubusercontent.com/56355682/232779493-553c6581-8162-4e6b-a139-7d3b3c594102.png)

* Após preencher os dados de destino e nome da rota clique na opção "Remessas"

![road5](https://user-images.githubusercontent.com/56355682/232779479-2d1e1f5d-a2fa-4f8f-a35b-e7fb0d5b3eba.png)

* Em seguida clique em "Visualizar Remessas"

![road6](https://user-images.githubusercontent.com/56355682/232779464-eb85d397-28b5-47c4-8bc2-ec4a471d85d6.png)

* Selecione a remessa à ser escolhida para a respectiva roteirização e clique em "Concluir"

![road7](https://user-images.githubusercontent.com/56355682/232779449-76b3bb2f-b857-4cb0-9fdb-29151bad78d3.png)

* Após a adição das remessas clique em "Avançar" para prosseguir com a roteirização

![road8](https://user-images.githubusercontent.com/56355682/232779434-fea96c55-05b8-4583-9dfa-42801e415433.png)

* Selecione a rota desejada para a distribuição automática e clique em "Avançar"

![road9](https://user-images.githubusercontent.com/56355682/232779641-6f6ef624-1675-4ca5-ad0b-7f9fc6c15bea.png)

* Agora com a rota criada vamos roteirizá-la, clique novamente no menu

![road10](https://user-images.githubusercontent.com/56355682/232779626-107ef498-33ce-49cd-9bf2-d2d9e06deca9.png)

* Selecione a opção "Roteirizar"

![road11](https://user-images.githubusercontent.com/56355682/232779589-08b33000-a7fd-43df-89df-882eea9ec96d.png)

* Selecione o veículo desejado para essa nova roteirização e clique em "Roteirizar"

![road12](https://user-images.githubusercontent.com/56355682/232779548-a0b022f6-1616-4dee-b5dd-7d9d19392d12.png)

Tudo pronto, sua rota foi roteirizada!
___
##### Listar rotas [GET]

> [GET] https://wayds.net:8081/integraway/api/v1/rota/capa?dataInicial=2022-12-01&dataFinal=2022-12-20

De posse de uma roteirização criada, com veículo montado e já sequenciado é possível recuperar os dados via chamadas de API.

Recomendamos que seja feito um controle dos veículos roteirizados, usando seu codigo único, por período de tempo via o endpoint, Sugerimos que o período escolhido seja o menor valor possível das rotas que vão ser mantidas
pelo sistema do cliente. **1 mês** é um valor que parece bastante razoável e atende a maioria dos clientes. No JSON da resposta, recebemos um Array com vários objetos. Cada objeto é referente a um dos veículos roteirizados dentro do período informado. O dado mais importante e relevante,
que é chave para buscar informações futuras, é a propriedade codigo, dentro de cada objeto.

* Parameters
    * dataInicial (required, date) - Data inicial para o intervalo de buscas de rotas
    * dataFinal (required, date) - Data final para o intervalo de buscas de rotas
    * motorista (optional, number) - Código do motorista
    * incluirFlagDel (optional, boolean) - Flag que indica se a rota está deletada
___
##### Listar rotas por código [GET]

> [GET] https://wayds.net:8081/integraway/api/v1/rota

De posse do **codigo** da rota de cada veículo, é possível, por fim, buscar todas as informações
de forma detalhada sobre aquela rota. Sendo necessário informar o código da rota e/ou um período com dataInicial (yyyy-MM-dd) e dataFinal (yyyy-MM-dd) válidos.

* Parameters
    * dataInicial (optional, date) - Data inicial para o intervalo de buscas de rotas
    * dataFinal (optional, date) - Data final para o intervalo de buscas de rotas
    * codigoRoteirizacao (optional, number) - Código da roteirização
    * codigoRota (optional, number) - Código da respectiva rota à ser retornada
    * placa (optional, string) - Placa do veículo