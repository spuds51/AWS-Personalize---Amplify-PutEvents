aws-personalize-github
Deben reemplazar los parametros del fichero aws-exports.js
Este es un ejemplo del fichero
```
// WARNING: DO NOT EDIT. This file is automatically generated by AWS Amplify. It will be overwritten.

const awsmobile = {
    "aws_project_region": "eu-west-1",
    "aws_appsync_graphqlEndpoint": "https://me4s6daeodjaowelhozes7spi.appsync-api.eu-west-1.amazonaws.com/graphql",
    "aws_appsync_region": "eu-west-1",
    "aws_appsync_authenticationType": "API_KEY",
    "aws_appsync_apiKey": "da2-asdasdjasidjasd8as8s",
    "aws_cognito_identity_pool_id": "eu-west-1:a9s8a98s-f367-4c9f-87c7-a99s8a9s8a9s8",
    "aws_cognito_region": "eu-west-1",
    "aws_user_pools_id": "eu-west-1_a98sa9s8a9s8",
    "aws_user_pools_web_client_id": "asdf7a9f9as7dfa9sd7fa97",
    "oauth": {},
    "aws_mobile_analytics_app_id": "a9d8a9d8a9sd8s9d8s9d8s9ds79dacv",
    "aws_mobile_analytics_app_region": "eu-west-1"
};


export default awsmobile;
```
Deben poner sus datos para poder interactuar con su aplicación, estos son inventado pero con la misma apariencia que los reales.

También teneis que añadir el tracking id en el fichero index.js:
```
// REQUIRED - The trackingId to track the events
      trackingId: 'TRACKINGID',
```
El treacking ID os lo proporciona AWS Personalize cuando creais un nuevo Tracking.

Los eventos los cogeis de tienda haciendo la siguiente llamada con Javascript en cada uno de los eventos que queráis configurar:
```
desApi.call('1', 'SET_EVENT_PRODUCT', '1', 'CLICK', '1', '','es-es');
```
Este es el orden de los parametros:
(shopId, functionOption, itemId, eventType, eventValue, category, catalog, stock, idCombination, name, offer, price, urlImage1, urlImage2, description, urlProduct)
No todos son obligatorios.

Para ejecutar:
````
npm install
npm run dev
`````
Para compilar:
````
npm run build
`````
