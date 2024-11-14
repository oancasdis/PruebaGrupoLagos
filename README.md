
# PruebaGrupoLagos

Este proyecto consiste en una aplicación con frontend y backend separados. La aplicación utiliza Angular para el frontend y Spring Boot para el backend. Aquí te mostramos cómo clonar, instalar dependencias, compilar y ejecutar el proyecto con Docker Compose.

## Requisitos previos

Asegúrate de tener instalados los siguientes programas en tu sistema:

- **Git**
- **Node.js** y **npm**
- **Maven**
- **JAVA 17**
- **Docker** y **Docker Compose**

## Instrucciones de configuración y ejecución

1. **Clonar el repositorio con los submódulos**

   Clona el repositorio y los submódulos con el siguiente comando:

   ```bash
   git clone --recurse-submodules <URL_DEL_REPOSITORIO>
   ```

2. **Instalar dependencias y compilar el frontend**

   Navega al directorio del frontend, instala las dependencias y compila el proyecto:

   ```bash
   cd PruebaGrupoLagosFrontend
   npm install
   ng build --configuration=production
   cd ..
   ```

3. **Compilar el backend**

   Navega al directorio del backend y compila el proyecto usando Maven:

   ```bash
   cd PruebaGrupoLagosBackend
   mvn clean package
   cd ..
   ```

4. **Ejecutar la aplicación con Docker Compose**

   Inicia los contenedores Docker del frontend y backend:

   ```bash
   sudo docker-compose up
   ```

## Acceso a la aplicación

Una vez que Docker Compose haya iniciado los contenedores, podrás acceder a la aplicación en tu navegador:

- **Frontend**: `http://localhost:4200`
- **Backend**: `http://localhost:8080`

## Notas adicionales

- Si necesitas detener los contenedores, usa `Ctrl+C` en la terminal o ejecuta `sudo docker-compose down`.
- Si realizas cambios en el código, vuelve a compilar y ejecuta los contenedores nuevamente para ver los cambios reflejados.

