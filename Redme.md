# Prueba Técnica Laravel Backend

Para la compilación del aplicativo debemos tener instalado en nuestros equipos el aplicativo [Docker](https://docs.docker.com/get-docker/) y seguir las siguientes instrucciones.

## Estructura de para el ambiente de desarrollo

1. Creamos una carpeta donde vamos almacenar todo nuestro proyecto (Eje: NewProject) y abrimos nuestra consola de comandos ubicandonos en dicha carpeta.

2. Clonamos el repositorio actual con la siguiente instrucción: `git clone https://github.com/Lucho2708/envlaravel` que corresponde al entorno de desarrollo que usaremos para nuestro proyecto de Laravel.

3. Clonamos el repositorio actual con la siguiente instrucción: `git clone https://github.com/Lucho2708/geducar` que corresponde a nuestro proyecto Laravel GEducar.

4. Ejcutamos el comando para construir nuestros contenedores de Doceker en nuestra consola de comandos: `docker-compose up -d` para levantar nuestro entorno de desarrollo.

5. Ejecutamos el siguiente comando de composer para actualizar Laravel: `composer update`

6. Ejecutamos el siguiente comando `cp .env.example .env`

7. Ejecutamos el siguiente comando `php artisan key:generate`

8. Con nuestro archivo `.env` generado, actualizamos las variables para la  conexión a la base de datos.

    `DB_HOST=mysql`

    `DB_PORT=3306`

    `DB_DATABASE=geducar`

    `DB_USERNAME=laravel`

    `DB_PASSWORD=secret`

9. Para finalizar, ejecutamos el siguiente codigo para que se generen las migraciones a la BD con los datos de prueba `docker-compose exec php /var/www/html/artisan migrate --seed`