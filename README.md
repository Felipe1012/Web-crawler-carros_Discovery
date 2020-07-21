# IBM Watson Discovery Demo: Web crawler carros

IBM Watson Discovery facilita la construcción de aplicaciones de exploración cognitivas y basadas en la nube que desbloquean los insights accionables que hay ocultos en los datos no estructurados. Esta demo utiliza usa una de las maneras para la ingesta de datos a Watson Discovery, un web crawler, para tomar información de tucarro.com y minar el contenido en cuanto a características de automóviles que se ofertan actualmente como lo son: precio, modelo, kilometraje, etc… 

## Arquitectura 🚀
![WhatsApp Image 2020-07-21 at 11 08 05 AM](https://user-images.githubusercontent.com/46906169/88103650-e6f2dc80-cb66-11ea-9963-32ef5e304002.jpeg)

### Pre-requisitos 📋

Para comenzar con esta demo es necesario:
- Tener una cuenta de IBM cloud, si aun no está creada en el siguiente enlace la puede crear [AQUI](https://cloud.ibm.com/).
- Crear un servicio de **Object storage**.
- Crear un servicio de **Watson Discovey**.
- Crear un servicio de **Natural Language Understanding**.
- Crear un servicio de **Knowlegde Studio**.

### Instalación 🔧

Es necesario cambiar las credenciales en el proyecto de los servicios nuevos que se creron en la cuenta personal de IBM cloud.
1. Credenciales Watson Discovery.
En el archivo ***params.json*** se encuentran las credenciales de los servicios cloud.

```
  "url": "URL DE SU SERVICIO",
  "iam_apikey": "APIKEY DE SU SERVICO"
```
![credenciales](https://user-images.githubusercontent.com/46906169/88110643-2bd04080-cb72-11ea-855b-bc3e31472421.png)

Es necesario ***environment_id*** que se obtienen por medio del siguiente comando cURL.
```
  curl -u "apikey":"{apikey}" "https://gateway.watsonplatform.net/discovery/api/v1/environments?version=2019-04-30"
```
Tambien necesario ***collection_id*** que se obtienen por medio del siguiente comando cURL.
```
  curl -X POST -u "apikey":"{apikey}" -H "Content-Type: application/json" -d '{
  "name": "test_collection",
  "description": "My test collection",
  "configuration_id": "{configuration_id}",
  "language": "en"
}' "https://gateway.watsonplatform.net/discovery/api/v1/environments/{environment_id}/collections?version=2019-04-30"
```

2. Credenciales Natural language Understanding.
En el archivo ***params.json*** se encuentran las credenciales de los servicios cloud.
```
"nl_api_key": "URL DE SU SERVICIO",
"nl_url": "APIKEY DE SU SERVICO",
```
![credenciales 2](https://user-images.githubusercontent.com/46906169/88112977-7d7aca00-cb76-11ea-8eb8-8766ba15d04f.png)

Es necesario ***model_id*** que se genera a partir del siguiente comando cURL.
```
curl --user "apikey:{apikey}" "{url}/v1/models?version=2019-07-12"

```
Las solicitudes de API requieren un parámetro de versión que tome una fecha en el formato **version=YYYY-MM-DD**. 

## Ejecutando las pruebas ⚙️

_Explica como ejecutar las pruebas automatizadas para este sistema_

### Analice las pruebas end-to-end 🔩

_Explica que verifican estas pruebas y por qué_

```
Da un ejemplo
```

### Y las pruebas de estilo de codificación ⌨️

_Explica que verifican estas pruebas y por qué_

```
Da un ejemplo
```

## Despliegue 📦

_Agrega notas adicionales sobre como hacer deploy_

## Construido con 🛠️

* [IBM Watson Discovery](https://cloud.ibm.com/docs/discovery?topic=discovery-sources#connectwebcrawl) 
* [IBM Natural Language Understanding](https://www.ibm.com/co-es/cloud/watson-natural-language-understanding) 

## Wiki 📖
* [Uso de Api Watson Discovery](https://cloud.ibm.com/apidocs/discovery)
* [Uso de Api NLU](https://cloud.ibm.com/apidocs/natural-language-understanding)
## Autores ✒️

Equipo tecnico Data & AI IBM Colombia

También puedes mirar la lista de todos los [contribuyentes](https://github.com/your/project/contributors) quíenes han participado en este proyecto. 

