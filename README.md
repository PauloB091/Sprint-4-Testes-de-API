# Sprint-4-Testes-de-API
# Testes de API com Postman

Este projeto tem como objetivo o estudo e a pratica de técnicas de
testes de API utilizando o Postman. O foco esta no design de testes,
na estruturacao de coleções e na validacao automatizada de respostas,
cobrindo cenarios funcionais, de contrato, de erros e de integridade
de dados.

## Sobre Testes de API

Testes de API consistem em validar diretamente as interfaces de
programação de aplicações, verificando se as requisiçoes e respostas
estao em conformidade com o contrato esperado. Esse tipo de teste e
fundamental porque as APIs conectam diferentes sistemas e camadas da
aplicação, sendo essenciais para garantir integração confiavel,
segurança e desempenho.

Principais tipos de testes de API:

-  Funcionais: verificam se os endpoints retornam os resultados
   esperados para cenarios validos.
-  Validacao de contrato: conferem status codes, cabeçalhos e
   estrutura do corpo da resposta.
-  Tratamento de erros: avaliam o comportamento da API frente a
   entradas invalidas, parametros ausentes e acessos nao autorizados.
-  Desempenho basico: medem tempos de resposta e identificam
   gargalos simples de processamento.

## Design de Testes para APIs

### Validacao de Contrato

A validação de contrato verifica se a resposta da API esta em
conformidade com o que foi acordado entre as partes. Isso inclui:

-  Codigos de status HTTP adequados para cada cenario.
-  Cabecalhos de resposta esperados, como Content-Type.
-  Estrutura do corpo da resposta, incluindo campos obrigatorios e
   opcionais.

### Testes Funcionais

Os testes funcionais validam os cenarios de sucesso e as regras de
negocio da aplicacao. Eles garantem que:

-  Requisicoes validas retornam os dados corretos.
-  Regras de negocio sao respeitadas nas respostas.
-  Fluxos principais funcionam de ponta a ponta.

### Testes de Erros e Limites

Esses testes verificam o comportamento da API em situacoes adversas:

-  Entradas invalidas e mal formatadas.
-  Parametros obrigatorios ausentes.
-  Acessos nao autorizados ou sem autenticação.
-  Valores nos limites aceitos pela aplicação.

### Testes de Integridade de Dados

Os testes de integridade de dados conferem se as informacoes
retornadas estao corretas e consistentes:

-  Tipos de dados dos campos da resposta.
-  Formatos esperados, como datas, numeros e strings.
-  Presenca de campos obrigatorios no corpo da resposta.

## Postman

O Postman e uma ferramenta amplamente utilizada para desenvolvimento e
testes de APIs. Os principais recursos utilizados neste projeto sao:

-  Coleçoes e organizacao em pastas: agrupamento de requisiçoes por
   funcionalidade ou recurso, facilitando a manutencao e a execução
   seletiva.
-  Variaveis: uso de variaveis de ambiente, globais e em nivel de
   colecao para parametrizar URLs, tokens e dados de entrada.
-  Scripts de pre-requisicao (pre-request scripts): executados antes
   da requisicao, permitindo gerar tokens, calcular valores e
   preparar dados dinamicos.
-  Scripts de teste (test scripts): executados apos a resposta,
   permitindo validar status, corpo, cabecalhos e tempo de resposta.
-  Assercoes com Chai no Postman: uso de pm.test e pm.expect para
   escrever assercoes legiveis e robustas.
-  Gerenciamento de ambientes: ambientes separados para
   desenvolvimento, homologação e produção, evitando mistura de
   configuracoes.

## Exemplos de Asserçoes

| Assercao | Descricao |
| --- | --- |
| Status code 200 | Valida requisicao bem-sucedida |
| Tempo de resposta < 1000ms | Verifica limite de desempenho |
| Corpo JSON possui propriedade | Verifica presenca de campo |
| Tamanho do array > 0 | Garante retorno de dados |
| Cabecalho Content-Type | Valida formato da resposta |
