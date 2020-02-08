# ⚙️⚙️⚙️⚙️ Instalar NodeJS * Version⚙️⚙️⚙️⚙️

## Descripción rápida 🚀:

Node.js es un lenguaje de programación ECMAScript que esta basado en el motor V8 de Google.


## Ques es NodeJS?

Node.js es un entorno en tiempo de ejecución multiplataforma, de código abierto, para la capa del servidor basado en el lenguaje de programación ECMAScript, asíncrono, con I/O de datos en una arquitectura orientada a eventos y basado en el motor V8 de Google.

## Beneficios:

+ Nos permite desarrollar aplicacion en el backend con un lenguaje muy utilizado llamado JS.
+ El consumo de memoria por session es menor a otros lenguaje comparados por C# JAVA entro otros.
+ La respuesta del servidores es mayor gracias a su control de respuesta multi hilo.

### Pasos para la instalacion:

```JS
// Actualisamos el apt-get
sudo apt-get update

// Instalamos CURL 
sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates

// Descargamos la version de node que deseamos
curl -sL https://deb.nodesource.com/setup_10.x | sudo bash

// Actualizamos el apt-get y instalamos yarn
sudo apt-get update && sudo apt-get install yarn

sudo apt update

// Ahora instalamos node.
sudo apt-get install nodejs
```

LINK: 

```

https://computingforgeeks.com/installing-node-js-10-lts-on-ubuntu-18-04-16-04-debian-9/

```
