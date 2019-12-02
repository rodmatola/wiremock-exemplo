# Wiremock exemplo


## Estrutura de pastas

Na raiz do projeto você encontra o arquivo `wire.jar`. Este arquivo é responsável por levantar o servidor local.

### mappings

Esta pasta contém as regras dos requests, endpoints e caminhos para os arquivios de responses.

Por exemplo: se a requisição é GET ou POST, qual o header ou body exato para se ter uma resposta, se o header ou body só precisa conter uma informação, e não ser extamente igual, e qual JSON responder para determindada requisição.

### __files

Esta pasta contém os responses no formato JSON mapeados na pasta `mappings`.

Sugestão: para não me perder, eu costumo dar o mesmo nome para os arquivos dentro do `mappings` e `__files`, com o prefixo `map` e sufixo `response` respectivamente para cada pasta. 

Exemplo:

O arquivo `map_login.json` aponta para o `login_response.json`


## Iniciando o Wiremock

Entre na pasta em que se localiza o `.jar` e execute o comando:

```
java -jar wire.jar --port [numero]
```

Substitua o [numero] pelo número da porta que deseja utilizar.

## Fazendo os testes

Você pode usar diversas ferramentas para testar se o mock/stub está funcionando, como o Postman, SoapUI, curl...

Eu indico o [Postman](https://www.getpostman.com/downloads/) pois, para mim, ele é bem mais amigável.

## Links de referência

- Documentação do [Wiremock](http://wiremock.org/docs/): aqui você encontra as informações de mais combinações para seu mock/stub, tanto para o `.jar` stand alone como comandos de Java.
- Repositório de [testes de contrato do Darling Lopes](https://github.com/DarlingL/contract_test_training), que serviu de base para fazer este. 
