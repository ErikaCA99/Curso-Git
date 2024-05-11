# Curso de GIT

<details><summary> <b> Clase 1 </b></summary>

## ¿Qué es Git?

> Git es un sistema de control de versiones, donde los cambios en el código son registrados por un historial en sus ficheros para saber quién y cuándo lo hizo.

<details><summary> :eyes: <b> Configurar el entorno</b></summary>

1. Cambiar los credenciales **globales**:

    ```sh
    git config --global user.name <tu_nombre>
	git config --global user.email <tu_email>
    ```

2. Cambiar credenciales **para un proyecto en concreto**:
    ```sh
    cd <tu_directorio>
    git config user.name <tu_nombre>
    git config user.email <tu_email>
    ```
    
3. Editor de código que se abre con Git:

    ```sh
    git config core.editor "code"
    ```
    > [!NOTE]\
    > En este caso se utiliza con **Visual Studio Code** pero se puede modificar a "atom", "subl", "nano",etc

4. Comprobar configuración de Git	:

    ```sh
    git config --list
    ```

</details>

## Ventajas

<div style="display:flex; justify-content: space-between; align-items: center;">
    <img src="https://cdn-icons-png.flaticon.com/512/5454/5454645.png" alt="Rendimiento" style="width: 70px;">
    <img src="https://cdn-icons-png.flaticon.com/512/2345/2345500.png" alt="Seguridad" style="width: 70px;">
    <img src="https://cdn-icons-png.flaticon.com/512/5201/5201492.png" alt="Flexibilidad" style="width: 70px;">
</div>

## Git posee 3 tipos de estados:
 
1.  **Modified:** Cuando un archivo tiene cambios marcados para ser confirmados y se encuentra en el directorio de trabajo.

2.  **Staged:** Los archivos modificados ya están marcados para ser confirmados en el repositorio local.

3.  **Commited:** Se crea un punto de guardado en el repositorio.

```mermaid
sequenceDiagram
Modified ->> Staged: Edit the file
Staged ->> Commited: Staged the file
Commited->> Modified: Commit
```

</details>

<details><summary> <b> Clase 2 </b></summary>

## Conceptos Principales

>El propósito principal de las ramas es el trabajo colaborativo en paralelo.

1. **Rama (Branch)**: una versión paralela del proyecto que se utiliza para desarrollar nuevas características o corregir errores sin afectar la rama principal.
2. **Rama principal (Main Branch)**: la rama predeterminada del proyecto, usualmente llamada "master".
3. **Rama de características (Feature Branch)**: una rama que se utiliza para desarrollar una nueva característica o funcionalidad.
4. **Rama de corrección (Hotfix Branch)**: una rama que se utiliza para corregir un error crítico en la rama principal.

## Flujo de trabajo

Crear una rama de características o corrección a partir de la rama principal.
Realizar cambios y commits en la rama creada.
Fusionar la rama creada con la rama principal cuando se complete el desarrollo.
Eliminar la rama creada una vez fusionada.

<details><summary><b> Ver Imagen</b></summary>
	
```mermaid
graph LR

Proyecto -- Rama principal --> B(( ))
B(( )) --> G(( ))
G(( )) --> H(( ))
B(( )) --> C(( ))
C(( )) --> D(( ))
C(( )) --> J(( ))
J(( )) --> L(( ))
L(( )) -.-> F(( ))
D(( )) --> E(( ))
E(( )) --> F(( ))
F(( )) --> K(( ))
K(( )) --> M(( ))
```
</details>

>Permite trabajar en diferentes versiones del proyecto de forma paralela.
Facilita la colaboración entre desarrolladores.
Permite revertir cambios si algo sale mal.

>Las ramas de Git son una herramienta poderosa para gestionar diferentes versiones de un proyecto. Al entender cómo crear, cambiar, fusionar y eliminar ramas, los desarrolladores pueden trabajar de forma más eficiente y colaborativa en proyectos complejos.
</details>


## Comandos

| Comando                     | Descripción                                                                |
| -------------------------   | -----------------------------------------------------------------          |
| `git init <nuevo_proyecto>` | Inicia un nuevo repositorio Git.                                           |
| `git status`                | Muestra el estado actual del proyecto.                                     |
| `git add`                   | Agrega todos los archivos al repositorio de Git.                           |
| `git restore --staged`      | Evita que los cambios en el área de preparación se incluyan en el commit.  |
| `git commit`                | Genera un registro del cambio realizado.                                   |
| `git log`                   | Muestra un historial de los commits realizados.                            |
| `git branch <nombre_rama>`  | Crear una rama este tiene diferentes complementos.                         |
| `git checkout <nombre_rama>`| Cambia la ubicación actual al "nombre_rama" con todos los cambios.         |
| `git merge <nombre_rama>`   | Fusiona una rama.				                           |
