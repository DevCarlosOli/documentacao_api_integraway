# ❗Considerações Iniciais

Durante as fases iniciais de implementação da API, será disponibilizado um token de acesso para nosso ambiente de **DESENVOLVIMENTO**.
Esse ambiente é destinado para fins somente de **TESTES**, portanto, recomendamos que o volume de dados inseridos para esse contexto seja limitado à uma quantidade que somente verifique se os endpoints implementados estão funcionando corretamente.
Nosso ambiente de desenvolvimento recebe atualizações esporádicas ao longo do tempo, podendo ocasionar em perda de dados já que o banco sempre é um espelho do ambiente de produção e para um primeiro momento, novas integrações ainda não estão inseridas nessa base, por isso ocorre eventualmente a perda de dados.
Há um limite para o cadastro de **Clientes** previamente estipulado.

⚠️ **Por tratar-se de um ambiente para testes, o servidor pode apresentar instabilidades.**

Posteriormente, após a finalização dos testes básicos, será fornecido o token para o ambiente de **PRODUÇÃO**, nesse contexto, já deverá ser cadastrado o volume real de dados.