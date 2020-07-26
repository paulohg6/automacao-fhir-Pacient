# Executando o projeto de automação


## Modificando Apenas a URL do servidor para executar os testes

Abra o arquivo variaveisGlobais.json contido dentro da pasta testes-pacient

dentro dele modifique a url que está em value, para a url do seu servidor.

```json

{
	"id": "4de0f774-3892-4cd7-8048-0fb8998bb525",
	"values": [
		{
            "key": "url_base",
            // Modifque o valor a baixo para a url do seu servidor
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

Após fazer apontar a url base para o seu servidor basta apenas entrar na pasta testes-pacient via cmd e executar o seguinte comando:

```javascript

newman run Pacient.json -r htmlextra --reporter-htmlextra-export ./results/report.html

```



## Importando a Colecion e Enviroment para o postman

Para importar o projeto no postman e executar os seus testes, você deve seguir os seguintes passos

Conforme a imagem:

 ![](/img/import1.png)

Clicar upload files e adicionar os arquivos JSON (*.json):
![](/img/import2.png)

pronto agora basta você modificar os testes da maneira que você desejar.

