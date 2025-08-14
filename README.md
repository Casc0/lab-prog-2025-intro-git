# 🎓 TP 0 - Introducción a Git

[cite_start]Este documento describe un ejercicio práctico para introducir el uso de Git y GitHub para el control de versiones[cite: 6]. [cite_start]Está dirigido a estudiantes del Departamento de Programación de la Facultad de Informática de la Universidad Nacional del Comahue[cite: 5].

***

## 🧐 Conceptos de Git

[cite_start]Basado en el diagrama provisto, aquí hay una explicación de algunos conceptos y comandos centrales de Git[cite: 7].

### Staging Area, Repositorio Local y Repositorio Remoto

* [cite_start]**Staging Area:** Este es un área intermedia donde preparas tus cambios antes de confirmarlos[cite: 13]. [cite_start]Te permite seleccionar qué cambios específicos quieres incluir en tu próximo **commit**[cite: 9].
* [cite_start]**Repositorio Local (**_**local repo**_**):** Es una copia completa del historial de tu proyecto, almacenada en tu computadora[cite: 14]. Contiene todos los commits que has realizado localmente.
* [cite_start]**Repositorio Remoto (**_**remote repo**_**):** Es una versión compartida de tu proyecto, generalmente alojada en un servicio como GitHub[cite: 15]. Funciona como un punto central para la colaboración, permitiendo que varios desarrolladores suban y bajen cambios desde una única fuente.

***

### `git add` vs. `git commit`

* [cite_start]`git add`: Este comando mueve los cambios de tu **directorio de trabajo** (`working directory`) al **área de preparación** (`staging area`)[cite: 16]. [cite_start]Es el primer paso en el proceso de **commit**, marcando los archivos para ser incluidos en la próxima confirmación[cite: 9].
* [cite_start]`git commit`: Este comando toma los cambios que están en el **área de preparación** y los registra permanentemente en tu **repositorio local** como un nuevo **commit**[cite: 17]. [cite_start]Cada **commit** tiene un ID único y un mensaje que describe los cambios que contiene[cite: 9].

***

## 🛠️ Ejercicio Práctico

### Configuración y Creación del Repositorio

1.  [cite_start]Cree una cuenta en GitHub usando su correo electrónico institucional[cite: 22].
2.  [cite_start]Localmente, configure su nombre de usuario y correo electrónico para Git[cite: 23].
3.  [cite_start]Cree un nuevo repositorio en GitHub llamado `lab-prog-2022-intro-git`[cite: 24].
4.  [cite_start]Clone este nuevo repositorio en su máquina local[cite: 25].

### Creación de Archivos y Commits

1.  [cite_start]Dentro de su repositorio local, cree un nuevo archivo llamado `concurrencia EnJava.md`[cite: 26].
2.  [cite_start]Agregue al menos dos commits a este archivo, describiendo las siguientes dos secciones[cite: 27]:
    * [cite_start]**Introducción:** Seleccione un mecanismo de sincronización de Java (como semáforos, monitores o bloqueos) y explíquelo en uno o dos párrafos[cite: 28, 29, 30, 31].
    * [cite_start]**Guía de Uso:** Detalle cómo usar el mecanismo elegido[cite: 32]. [cite_start]Por ejemplo, si elige semáforos, explique cómo importar la clase y qué métodos usar (por ejemplo, `acquire()` y `release()`)[cite: 39].

### Ramificación y Pushing

1.  [cite_start]Después de crear sus commits, use `git push` para subir sus cambios locales a su repositorio remoto en GitHub[cite: 40].
2.  [cite_start]Localmente, cree una nueva rama llamada `feature/concurrencia-en-java`[cite: 41].
3.  [cite_start]En esta nueva rama, cree una carpeta llamada `ejemplo` y agregue uno o más archivos Java que contengan un ejemplo funcional del mecanismo de sincronización que describió[cite: 42, 43].
4.  [cite_start]Cree al menos un commit para estos nuevos archivos[cite: 42].
5.  [cite_start]Suba los cambios de esta nueva rama a GitHub[cite: 44].

***

### Revisión y Colaboración

1.  [cite_start]Ejecute un comando para ver las diferencias entre su rama `feature/concurrencia-en-java` y la rama principal (`main`), y adjunte la salida[cite: 45].
2.  [cite_start]Ejecute un comando para ver el historial de todos los commits de esta rama[cite: 46].
3.  [cite_start]En GitHub, cree un **Pull Request** desde su rama `feature/concurrencia-en-java` a la rama `main` del repositorio[cite: 47].
4.  [cite_start]Agregue una descripción adecuada de los cambios introducidos en su **Pull Request**[cite: 48].

***

## 🔄 Explicación del Modelo de Ramificación de Git

La imagen provista en la página 2 ilustra un modelo común de ramificación de Git. [cite_start]Este modelo utiliza varios tipos de ramas para gestionar el proceso de desarrollo[cite: 1, 2, 3, 4, 5, 33, 34, 35, 36, 37, 49].

* [cite_start]**`Master` (o `main`):** Esta rama contiene el código estable y listo para producción[cite: 54]. [cite_start]Los commits aquí suelen estar etiquetados con números de versión (ej. v1.0)[cite: 52].
* [cite_start]**`Develop`:** Esta es la rama de integración principal para el desarrollo continuo[cite: 57]. Todas las nuevas características y correcciones de errores se fusionan finalmente en esta rama.
* [cite_start]**Ramas de `Feature`:** Estas son ramas temporales creadas para desarrollar nuevas funcionalidades[cite: 58]. Una vez que una característica está completa, se fusiona en la rama `Develop` y la rama de `feature` se elimina.
* [cite_start]**Ramas de `Release`:** Estas ramas se crean a partir de `Develop` cuando se prepara un nuevo lanzamiento[cite: 56]. Se utilizan para las correcciones de errores finales y las pruebas antes de fusionarse tanto en `Master` como en `Develop`.
