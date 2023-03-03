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

