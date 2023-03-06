# NestJS

Created by: Kenny Eduard Vercaemer González
Last edited by: Alejandro Mtz. Luna
Tags: Technology, Todo
URL: https://docs.nestjs.com/

# ¿Qué es NestJs?

NestJS es un marco de trabajo para Node.js que utiliza TypeScript y se basa en el patrón de arquitectura de servidor Modelo-Vista-Controlador (MVC) y el patrón de inyección de dependencias (IoC). Esto lo hace altamente escalable y fácil de mantener.

## Pros

### **1. Modularidad**

NestJS se basa en módulos, lo que facilita la creación de aplicaciones escalables y fáciles de mantener. Los módulos permiten una mejor organización del código y una fácil separación de la lógica de negocio.

### **2. Patrones de diseño**

NestJS utiliza patrones de diseño como el patrón de inyección de dependencias (IoC) y el patrón Modelo-Vista-Controlador (MVC), lo que hace que la aplicación sea más fácil de entender, mantener y escalar.

### **3. Soporte para TypeScript**

NestJS está construido sobre TypeScript, lo que proporciona una mejor legibilidad y facilidad de mantenimiento del código. TypeScript también proporciona una mayor seguridad al permitir la detección temprana de errores en tiempo de compilación.

### **4. Amplia comunidad de desarrolladores**

NestJS tiene una gran comunidad de desarrolladores y contribuidores que proporcionan soporte, documentación y herramientas adicionales. También hay una gran cantidad de bibliotecas de terceros disponibles para su uso con NestJS.

### **5. Integración con otros marcos de trabajo**

NestJS se integra fácilmente con otros marcos de trabajo y bibliotecas de JavaScript, como Express y Fastify, lo que permite una mayor flexibilidad y personalización en el desarrollo de aplicaciones.

## Contras

### **1. Curva de aprendizaje**

NestJS puede tener una curva de aprendizaje pronunciada para aquellos que no están familiarizados con TypeScript, patrones de diseño y la estructura de módulos. Sin embargo, esto puede ser superado con la práctica y la experiencia.

### **2. Sobrecarga**

NestJS puede tener una sobrecarga en la creación de aplicaciones más simples, ya que está diseñado para manejar aplicaciones más grandes y complejas. Esto puede hacer que la creación de aplicaciones más simples sea menos eficiente.

### **3. Dependencia de Node.js**

NestJS es dependiente de Node.js, lo que puede ser un obstáculo para aquellos que prefieren utilizar otros lenguajes de programación o marcos de trabajo.

### **4. Tamaño de la aplicación**

NestJS puede hacer que el tamaño de la aplicación sea más grande debido a la necesidad de incluir las bibliotecas y dependencias adicionales. Sin embargo, esto puede ser mitigado mediante el uso de herramientas de empaquetamiento y optimización de código.

En resumen, NestJS ofrece muchos beneficios, como modularidad, patrones de diseño, soporte para TypeScript, una gran comunidad de desarrolladores y flexibilidad para integrarse con otros marcos de trabajo. Sin embargo, también tiene algunas desventajas, como una curva de aprendizaje pronunciada, sobrecarga para aplicaciones más simples, dependencia de Node.js y un posible aumento en el tamaño de la aplicación.

# **Instalación**

Para instalar NestJS, puedes utilizar el comando de Node Package Manager (npm):

`npm i -g @nestjs/cli`

# **Crear un nuevo proyecto**

Puedes crear un nuevo proyecto utilizando el comando 

**`nest new <nombre del proyecto>`**

Por ejemplo:

`nest new mi-proyecto`

Esto creará un nuevo proyecto de NestJS con una estructura básica de archivos y carpetas.

# **Crear un controlador**

Los controladores son responsables de manejar las solicitudes HTTP entrantes. Puedes crear un controlador utilizando el comando

 **`nest generate controller <nombre del controlador>`**

Por ejemplo:

```less
nest generate controller miControlador
```

Esto creará un archivo **`miControlador.controller.ts`** en la carpeta **`src`** con un controlador básico.

# **Crear un servicio**

Los servicios son responsables de manejar la lógica de negocio de la aplicación. Puedes crear un servicio utilizando el comando **`nest generate service <nombre del servicio>`**. Por ejemplo:

```less
nest generate service miServicio
```

Esto creará un archivo **`miServicio.service.ts`** en la carpeta **`src`**con un servicio básico.

# **Inyectar dependencias**

NestJS utiliza el patrón de inyección de dependencias para manejar las dependencias entre los diferentes componentes de la aplicación.

Puedes inyectar dependencias en un controlador o servicio utilizando el decorador **`@Injectable()`** y el decorador **`@Inject()`**. Por ejemplo:

```tsx
import { Injectable, Inject } from '@nestjs/common';
import { MiServicio } from './miServicio.service';

@Injectable()
export class MiControlador {
  constructor(@Inject('MiServicio') private readonly miServicio: MiServicio) {}

  // ...
}
```

Aquí, estamos inyectando el servicio **`MiServicio`** en el controlador **`MiControlador`**.

# Configuración

Puedes configurar tu aplicación utilizando el archivo **`app.module.ts`.**

Aquí es donde importas todos los módulos necesarios y los agregas a la lista de proveedores. Por ejemplo:

```tsx
import { Module } from '@nestjs/common';
import { MiControlador } from './miControlador.controller';
import { MiServicio } from './miServicio.service';

@Module({
  controllers: [MiControlador],
  providers: [
    {
      provide: 'MiServicio',
      useClass: MiServicio,
    },
  ],
})
export class AppModule {}
```

Aquí, estamos importando el controlador **`MiControlador`** y el servicio **`MiServicio`**. También estamos agregando el servicio a la lista de proveedores, utilizando el nombre **`MiServicio`**.

# **Ejecutar la aplicación**

Para ejecutar la aplicación, puedes utilizar el comando **`npm run start`**. Esto iniciará el servidor en el puerto por defecto (3000).

# Recomendaciones para el uso de NestJs

## **1. NestJS Snippets**

Esta extensión proporciona una gran cantidad de snippets útiles para escribir código de NestJS. Simplifica la escritura de código al proporcionar atajos de teclado para bloques de código comunes, como controladores, servicios, módulos y más.

## **2. NestJS Explorer**

Esta extensión agrega una vista de árbol a Visual Studio Code que muestra la estructura de su proyecto NestJS, lo que facilita la navegación por los diferentes archivos y carpetas de su aplicación.

<aside>
💻

</aside>

---

# Documentación y recursos

<aside>
📆 Documentación Oficial NestJS

</aside>

[Documentation | NestJS - A progressive Node.js framework](https://docs.nestjs.com/)