# Guía de uso del Job en Jenkins y Configuración de Webhook y Pipeline para CI/CD de Node.js

Este documento proporciona una guía detallada sobre cómo utilizar el Job en Jenkins para configurar un webhook en un repositorio de GitHub y crear un pipeline básico para ejecutar un build y realizar pruebas en un proyecto Node.js. A continuación se muestra un diagrama para el entendimiento del flujo del evento que ejecuta el job automatico al hacer un push o un pull request.

![Diagrama](https://github.com/1wil1/nodejs-helloworld-api/assets/109010471/13390cb8-dbae-439e-9a68-83219ac3004e)


## Pasos para utilizar el Job

### 1. Iniciar el Job en Jenkins

1. Inicie sesión en Jenkins con sus credenciales.
2. Vaya al tablero de Jenkins y seleccione el proyecto que contiene el Job.
3. Haga clic en "Build Now" para ejecutar el Job.

### 2. Ingresar los parámetros requeridos

1. En el menú desplegable del Job, seleccione "Build with Parameters".
2. Complete los siguientes campos:
   - **Login:** Ingrese un identificador único compuesto por nombre y apellido para el usuario.
   - **NombreApellido:** Ingrese el nombre y apellido del usuario.
   - **Departamento:** Seleccione el grupo correspondiente al área del usuario entre las opciones disponibles: contabilidad, finanzas o tecnología.
3. Haga clic en "Build" para iniciar el Job con los parámetros proporcionados.

### 3. Revisar el resultado

Una vez completado el Job, revise el resultado en la salida de Jenkins. Se mostrará un mensaje con la contraseña temporal generada para el usuario creado.

## Notas adicionales

- Este Job utiliza herramientas estándar de Linux como `useradd`, `groupadd`, `chpasswd` y `chage` para realizar las tareas especificadas.
- La contraseña temporal generada se mostrará en la salida de Jenkins para que el administrador pueda comunicársela al usuario correspondiente.
- Se recomienda cambiar la contraseña temporal en el primer inicio de sesión del usuario por motivos de seguridad.

Con esta guía, podrá utilizar el Job en Jenkins de manera efectiva para crear grupos y usuarios en su sistema Linux. Si tiene alguna pregunta o problema, no dude en comunicarse con el administrador del sistema o el equipo de soporte técnico.
