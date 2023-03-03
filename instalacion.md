### Pasos para usar angular en el pc:

1.Instalar NodeJS desde https://nodejs.org/es/download/

2.instalar angular cli con el siguiente comando

```
npm install -g @angular/cli
```

>En este caso se uso la version 9.5.1

3.Despues en la consola pondremos el siguiente comando para crear el cliente con angular

```
ng new (nombre)
```

### Pasos para hacer el proyecto
>Como consejo se recomienda iniciar el proyecto apenas comenzar y ver que inicie bien
```
ng serve--o
```
#### 1. usar Bootstrap (opcional) 
>primero iremos a la siguiente pagina https://getbootstrap.com/
luego pondremos el siguiente comando para instalarlo en el proyecto
>nota el comando cambiara dependiendo la version actual de bootstrap, por lo cual se aconseja meterse en el link y buscar el comando
```
npm install bootstrap@5.3.0-alpha1
```
>Luego iremos al archivo angular.json en la carpeta cliente y buscamos donde diga styles, normalmente estara en la linea 27, ahi pondremos lo siguiente:
```
"node_modules/bootstrap/dist/css/bootstrap.css"
```

### 2. Generar componentes
Para generar los componentes se usa el comando
```
ng g c components/Nombre-del-componente
```
Para este proyecto usaremos
- crear-producto
- listar-producto

### 3. Generar servicios
Para generar los servicios se usa el comando
```
ng g s services/Nombre-del-servicio
```
Para este proyecto usaremos
- productoService

### 4. Crear Carpeta models
A nivel de components y services crearemos una carpeta llamada **Models**
dentro de models creamos un archivo llamado producto.ts
>El codigo de producto.ts lo encontraran en la carpeta models del proyecto o [ACA](https://github.com/notsapien/Clases-de-Richard/blob/main/cliente-angular/src/app/models/producto.ts)

### 5. Rutas
en [app-routing.module.ts](https://github.com/notsapien/Clases-de-Richard/blob/main/cliente-angular/src/app/app-routing.module.ts) buscaremos routes y pondremos lo siguiente
```
  {path:'',component:ListarProductoComponent},
  {path:'crear-producto',component:CrearProductoComponent},
  {path:'editar-producto/:id',component:CrearProductoComponent},
  {path:'**',pathMatch:'full',redirectTo:''}
```

hay que asegurarnos que en [app.component.html](https://github.com/notsapien/Clases-de-Richard/blob/main/cliente-angular/src/app/app.component.html) se encuentre el <router-outlet></router-outlet>

### 6. UiGradients y fontsAwesome(opcional)

En caso de que queramos usar UiGradients (que es para añadir fondos en degradado) usar el siguiente link 
https://uigradients.com/

Para fontawesome buscaremos en internet fontawesome cdn (lo usaremos para iconos) el link del cdn esta aca
https://cdnjs.com/libraries/font-awesome

y el cdn actual es este
>https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.3.0/css/all.min.css
 y lo ponemos en el index.html

 ### 7. Diseño
 Los siguientes pasos seran empezar a hacer el html y css de los componentes a usar en este caso
 Crear-producto y listar-producto

### 8. Mongodb

Lo primero que haremos sera ir a la pagina principal de Mongodb e iniciar sesion
En la pagina crearemos una base de datos, le ponemos cualquier nombre, creamos el usuario y contraseña
>para este proyecto el usuario es root y la contraseña es 1234
instalaremos monog db compass
>para este proyecto se usa la version 1.33.1 (el nombre del archivo es mongodb-compass-1.33.1-win32-x64.exe
) se puede encontrar en el siguiente link https://github.com/mongodb-js/compass/releases/tag/v1.33.1

en el mongo db compass ponemos lo siguiente
mongodb+srv://root:\<password\>@projectmeanwithme.c9qexxl.mongodb.net/
y cambiaremos \<password\> por la contraseña del proyecto

### 9.Nodejs
lo primero sera crear la carpeta servidor y desde la terminal poner
>npm init
esto nos creara un package.json

lo siguiente sera instalar las dependencias

primero nodemon (la -D es porque es en desarollo)
>npm i -D nodemon

luego instalaremos las siguientes
>npm i express dotenv cors mongoose

para que funcione nodemon iremos al package.json y en script pondremos lo siguiente
>"dev":"nodemon ."

luego crearemos el index.js y pondremos algunas cosas

a nivel del index.js crearemos las carpetas
-routes
-models
-controllers
-config


