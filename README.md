# express_migrate

Desafío  de hoy: migraciones

 Al final de la clase esta explicado el desafío de hoy. 

 Leer esta documentación. https://sequelize.org/docs/v6/other-topics/migrations/     https://www.notion.so/larnu/Migraciones-con-express-28124929d0e943ddb711c25441445fbf
 Leer este código (la parte de las migraciones y el README)  https://github.com/larnu-bootcamp/express_crud
 Hacer las migraciones en su código, y ver como afecta su base de datos.

instalar la CLI de Sequelize:
# install packages 
npm install --save-dev sequelize-cli

Para crear un proyecto vacío, deberá ejecutar el init comando
crear 
npx sequelize-cli init

Esto creará las siguientes carpetas

config, contiene un archivo de configuración, que le dice a CLI cómo conectarse con la base de datos
models, contiene todos los modelos para su proyecto
migrations, contiene todos los archivos de migración
seeders, contiene todos los archivos semilla



migrations, contiene todos los archivos de migración
seeders, contiene todos los archivos semilla
Antes de continuar, necesitaremos decirle a la CLI cómo conectarse a la base de datos. Para hacer eso, abramos el archivo de configuración predeterminado config/config.json. Se ve algo como esto:

{
  "development": {
    "username": "postgres",
    "password": 123456,
    "database": "qroll",
    "host": "localhost",
    "dialect": "postgres"
  },
  
  Vamos a crear un modelo llamado Clases.

npx sequelize-cli model:generate --name Clases --attributes firstName:string,lastName:string,email:string



Ejecutando Migracion

Hasta este paso, no hemos insertado nada en la base de datos. Acabamos de crear el modelo necesario y los archivos de migración para nuestro primer modelo, User. Ahora, para crear realmente esa tabla en la base de datos, debe ejecutar el db:migratecomando.

npx sequelize-cli db:migrate

[![2.png](https://i.postimg.cc/C1mz2HYx/2.png)](https://postimg.cc/r0RV04KB)

[![1.png](https://i.postimg.cc/C5sY2vSZ/1.png)](https://postimg.cc/ctCVgBKZ)
