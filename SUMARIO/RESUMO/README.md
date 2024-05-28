# 🧭Resumo

O fluxo da integração começa inicialmente pela importação dos **CLIENTES** para a plataforma da Way Data. Em seguida, o próximo passo é a importação dos pedidos (chamados de **REMESSAS** inicialmente), que só serão integrados mediante a terem seus respectivos clientes cadastrados.

Estando os dados anteriores importados, a partir de agora o roteirista consegue criar uma **ROTEIRIZAÇÃO**, na qual ele pode utilizar as **REMESSAS** importadas, que, ao serem incluídas na Roteirização passam a ser **PEDIDOS** dentro da plataforma da Way Data.

Um pedido importado que não se encontra em nenhuma **ROTEIRIZAÇÃO** é denominado **REMESSA**, e, uma vez, importado para uma Roteirização, ele é chamada de fato de **PEDIDO**.

Vale ressaltar que uma Roteirização pode ter uma ou várias Rotas. Uma rota é composta por um veículo, um motorista (opcional) e um ou vários pedidos.

Após a criação da roteirização e faturamento dos pedidos é necessário fazer o processo de **CONSOLIDAÇÃO**.

Nessa etapa, a empresa verifica se os pedidos e itens faturados batem com os listados na roteirização e caso exista uma discrepância, é realizada uma alteração nos respectivos pedidos visando a conformidade entre os pedidos **faturados** e **roteirizados**.

Por fim, é possivel que o cliente busque o **STATUS DA ENTREGA** para preencher o seu próprio ERP, por meio do endpoint de rotas.

É importante ressaltar que todo o processo deve ser implementado primeiramente no **ambiente de desenvolvimento** e, ao finalizar esta etapa e validar se está tudo funcionando devidamente, é disponibilizado o token do **ambiente de produção**.