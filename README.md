## Testes

Os testes estão disponíveis na pasta [testes-pacient](./testes-pacient). 

## Processo de criação de testes

Descreva como criar os testes nesta seção.

## Configuração para execução dos testes

Modifique o arquivo **variaveisGlobais.json**, ilustrado abaxio, para apontar para o servidor a ser testado.
A propriedade de chave **value** deve indicar a URL do servidor. 

```json
{
	"id": "4de0f774-3892-4cd7-8048-0fb8998bb525",
	"values": [
		{
            "key": "url_base",
			"value": "http://hapi.fhir.org/baseDstu3",
			"enabled": true
		}
	],
	"name": "My Workspace Globals",
	"_postman_variable_scope": "globals",
	"_postman_exported_at": "2020-07-24T18:37:00.164Z",
	"_postman_exported_using": "Postman/7.28.0"
}

```

Após a alteração, execute o seguinte comando:

```bash
newman run Pacient.json -e variaveisGlobais.json -r htmlextra --reporter-htmlextra-export ./results/report.html
```

Este comando produz no formato HTML os resultados da execução dos testes definidos no arquivo **Pacient.json**.


## Importando a Collecion e Enviroment para o postman

Para importar o projeto no postman e executar os seus testes, você deve seguir os seguintes passos

Conforme a imagem:

 ![](/img/import1.png)

Clicar upload files e adicionar os arquivos JSON (*.json):
![](/img/import2.png)

pronto agora basta você modificar os testes da maneira que você desejar.

