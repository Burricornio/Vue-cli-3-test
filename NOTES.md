# Notas Vue cli 3

## Vue cli 2 vs Vue cli 3
Al instalar Vue cli 3 el comando 'vue init' deja de funcionar. Para que vuelva a funcionar hay que instalar: npm install -g @vue/cli-init en el equipo. 
De esta manera pueden convivir 'vue create' y 'vue init'.

## Vue cli 2 vs Vue cli 3
Crear nuevo proyecto: ```vue create``` o utilizar la interface ```vue ui```
Puedes ir configunado el proyecto a la carta o utilizar un preset anterior.

## Estructura proyecto.
La estructura es muy parecida. Una diferencia importante es que puedes añadir plugins. No hay que instalarlo todo por nopm o yarn.

## Instalar plugin

1. Para instalar un plugin en el proyecto ```vue add [nombre plugin]``` --> Ej: vue add vuetify

2. Para buscar info de un plugin: vue-cli-plugin-...

## Variables de entorno

1.  Se crean ficheros .env [.env.development, .env.development, .env.production, .env.test]

2. En estos ficheros declaramos vatiables de tipo VUE_APP_URL = https://api.com para posteriormente hacer referencia a ellas con ```process.env.[nombre variable]``` --> Ej: process.env.VUE_APP_URL

3. Es importante que el nombre de variable empiece por VUE_APP_

## Construyendo el proyecto

1. Se pueden lanzar los scripts con yarn, npm o vue si tenemos intalado el vue-cli-service a nivel global en el equipo

2. Se pueden crear scripts en el package json. El script para development no viene preconfigurado (se utiliza el serve). Para crearlo: ```"build:development": "vue-cli-service build --mode development"```

## Nueva opción de prototipado
Instalando ```npm install -g @vue/cli-service-global```podemos ver los componentes simplemente escribiendo ```vue serve [nombre fichero]```en la consola.

## Modo producción (build)
Existen tres tipos de despliegue para producción:

1. Vue app - Comando: vue build --target app. Es el modo por defecto. Construye el bundle para subir a procucción como un proyecto de vue. Incluye el framework en sí.

2. Vue Library - Comando: vue build --target lib. Sirve para crear librerías de componente Vue. No incluye el framework. Para utilzar la librería, hría que importarla dentro de un proyecto de Vue.

3. Web Component - Comando: vue build --target wc. Crea un web component independiente que puede ser utilizado en cualquier otro framework o en un simple .html

* Instalo http-server a modo global en el equipo para hacer un cd/dist/ --> http-server

## Vue UI
Comando: vue ui. La nueva versión de Vue cli incluye una interface gráfica.
