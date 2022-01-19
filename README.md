
# DIO - AWS Conceitos - Bootcamp Eduzz

Função Lambda desenvolvida durante o Bootcamp da Eduzz na plataforma DIO.
Consiste basicamente de uma API para cadastro básico de um produto para demonstrar a utilização da integração de serviços da AWS

## Tech Stack

- AWS
- Lambda
- API Gateway
- Dynamo DB

### _AWS_

A Amazon Web Services oferece serviços de computação em nuvem confiáveis, escaláveis e acessíveis.
<br>
<br>

### _Lambda_

O AWS Lambda é um serviço de computação que executa suas aplicações em um modelo serveless, onde você pode desenvolver sem a necessidade de se preocupar com servidores.

É possível utilizar as principais linguagens do mercado, como Java, Pyhton, Node.JS, .NET Core, e Go, podendo expandir essa lista para outras linguagens utilizando um custom Lambda Runtime, adicionando suporte até para COBOL!

Além disso, com o Lambda você só paga pelo o que você consumir para executar sua função. Não é necessário pagar por capacidade ociosa e, por fim você pode publicar sua aplicação de forma mais ágil. 

Com o Lambda podemos construir aplicações baseadas em pequenas funções, com uma responsabilidade única iniciada a partir de eventos. Essa é a principal diferença com uma aplicação web, pois nosso código implementa somente o que é necessário para ser executado. Podemos por exemplo, responder a uma requisição HTTP, ou redimensionar uma imagem salva no S3, ou processar uma mensagem enviada numa fila do SQS, com o mínimo de código possível.
<br>
<br>

### _API Gateway_

O Amazon API Gateway é um serviço gerenciado que permite que desenvolvedores criem, publiquem, mantenham, monitorem e protejam APIs em qualquer escala com facilidade. APIs agem como a “porta de entrada” para aplicativos acessarem dados, lógica de negócios ou funcionalidade de seus serviços de back-end. Usando o API Gateway, você pode criar APIs do RESTful e APIs do WebSocket que habilitam aplicativos de comunicação bidirecionais em tempo real. O API Gateway dá suporte a cargas de trabalho conteinerizadas e sem servidor, além de aplicativos da web.
<br>
<br>

### _DynamoDB_

O Amazon DynamoDB é um serviço de banco de dados NoSQL totalmente gerenciado que fornece uma performance rápida e previsível com escalabilidade integrada. O DynamoDB permite que você transfira os encargos administrativos de operação e escalabilidade de um banco de dados distribuído. Assim, você não precisa se preocupar com provisionamento, instalação e configuração de hardware, replicação, correção de software nem escalabilidade de cluster. Além disso, o DynamoDB oferece criptografia em repouso, o que elimina a carga e a complexidade operacionais envolvidas na proteção de dados confidenciais.
<br>
<br>

## Endpoints

:GET {url-api-aws}/items - retorna todos os itens cadastrados.

:POST {url-api-aws}/items - cadastra um produto.<br>
  body JSON: {
    id: string,
    name: string,
    manufacturer: string,
    price: number
  }

:GET {url-api-aws}/items/:id - retorna um produto pelo :id especificado.

:PUT {url-api-aws}/items/:id - atualiza o valor de um produto por id.<br>
  body JSON {
    price: number
  }

:DELETE {url-api-aws}/items/:id } - deleta o produto especificado pelo :id.





