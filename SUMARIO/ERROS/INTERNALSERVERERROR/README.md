# 😵‍💫Retorno 500: Internal Server Error

Caso esse retorno seja apresentado, é possível que alguma falha não prevista tenha acontecido em nossos servidores.

Mesmo assim, a API retornará uma HASH que poderá ser usada para entrar em contato com a Way Data Solution.

Esta sequência de caracteres contém toda a informação necessária para que nossa equipe solucione o problema da forma mais rápida possível.

Na maioria dos casos, como apresentado abaixo, o erro também é descritivo, podendo ser
solucionado pelo próprio cliente, sem a necessidade de um suporte avançado.

Em outros casos, a propriedade razao será **restrita**, e o cliente deverá **entrar em contato**.

```JSON
    {
        "mensagem": "Erro ao inserir cliente",
        "razao": "Endereço não encontrado",
        "hash": "0226634341824fe575d1922458082ca9789aaa256b6f75d02a27c7403d186f96",
        "traceId": "00-0fd6bb53869e78489d479fe82b823aa0-1177d8aee73d374d-00",
    }
```