---
theme: jekyll-theme-leap-day
---

[Regresar](/DAWM-2022/)

## NPM

### Proxy

* Al ejecutar desde la línea de comandos `npm install @angular/cli`
	+ **Problema:** no continúa la descarga de módulos
	  ![comandos](imagenes/comandos.png)
	+ **Solución:**
		- Agregue un proxy para la petición de módulos
		```
		npm config set proxy <URL-PROXY>
		npm config set https-proxy <URL-PROXY>
		```

### Comandos executables
* Al ejecutar desde la línea de comandos `ng`
	+ **Problema:** no se reconoce el comando ng luego de instalar `npm install @angular/cli`
	![ng not found](imagenes/ngnotfound.png)
	+ **Solución:**
		- Liste la ubicación por defecto que npm reconoce los comandos instalados
		```
		npm config get prefix
		```
		- Agregue la ruta a la variable de entorno `PATH`
		- Reinice el cmd, de ser necesario.

## Angular

* Al ejecutar desde la línea de comandos `ng serve`
	+ **Problema:**   
		```
		Can't resolve '../yyy/zzz/image.jpg' in file ...
		``` 
	+ **Solución:**
		- Mueva la estructura de archivos con la imagen a la ruta `src/assets`
		- Cambie la referencia por `'assets/yyy/zzz/image.jpg'` en el archivo