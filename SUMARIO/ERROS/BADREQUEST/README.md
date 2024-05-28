# 🤦‍♂️Retorno 400: Bad Request

Este retorno representa uma falha de validação nos models ou parâmetros enviados. 

Seu retorno é descritivo, indicando exatamente onde está o problema, até mesmo quando o envio contém uma lista de objetos.

Abaixo encontra-se um exemplo de falha de validação.

```JSON
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0fd6bb53869e78489d479fe82b823aa0-1177d8aee73d374d-00",
    "errors": {
        "CnpjEmissor": [
            "O CNPJ do Emissor está mal formatado (nn.nnn.nnn/nnnn-nn)"
        ]
    }
}
```