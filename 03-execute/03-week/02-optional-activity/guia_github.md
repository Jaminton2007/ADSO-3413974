# Guía de GitHub para Principiantes

## Introducción

Git es un sistema de control de versiones: un programa que registra cada cambio que haces en tus archivos a lo largo del tiempo. Esto te permite volver a versiones anteriores, trabajar en equipo sin pisarte con otros y mantener un historial completo de tu proyecto.

GitHub es una plataforma en internet que usa Git por debajo. Te permite guardar tus proyectos en la nube, compartirlos con otras personas y colaborar en equipo.

En resumen: **Git** es la herramienta, **GitHub** es el sitio web donde guardas y compartes tu trabajo.

---

## 1. Conceptos Fundamentales

Antes de empezar a usar GitHub, es importante entender algunos términos que aparecerán constantemente.

**Repositorio**: Es la carpeta de tu proyecto gestionada por Git. Contiene todos los archivos del proyecto y el historial de cada cambio que se ha hecho en ellos.

**Commit**: Es una fotografía del estado de tus archivos en un momento determinado. Cada vez que terminas un cambio y lo confirmas, creas un commit. Los commits se apilan en orden cronológico, formando el historial del proyecto.

**Branch (rama)**: Es una línea de trabajo independiente. Por defecto existe una rama principal llamada `main`. Cuando quieres desarrollar algo nuevo sin afectar el código que ya funciona, creas una rama separada, trabajas en ella, y luego la unes de vuelta.

**Merge**: Es el proceso de unir los cambios de una rama con otra.

**Pull Request**: Cuando trabajas con otras personas, un pull request es una propuesta formal de fusionar tus cambios al proyecto. Permite que el equipo revise el código antes de aceptarlo.

**Clone**: Copiar un repositorio que está en GitHub a tu computadora para trabajar en él localmente.

**Push**: Subir los commits de tu computadora al repositorio en GitHub.

**Pull**: Traer los cambios que están en GitHub a tu computadora.

---

## 2. Instalación y Configuración

### Instalar Git

Descarga Git desde https://git-scm.com y sigue el proceso de instalación para tu sistema operativo.

Para verificar que quedó instalado correctamente, abre una terminal y ejecuta:

```bash
git --version
```

Si muestra un número de versión, la instalación fue exitosa.

### Configurar tu nombre y correo

Git necesita saber quién eres para asociar tu identidad a cada commit. Ejecuta estos dos comandos en la terminal, reemplazando los valores:

```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@ejemplo.com"
```

Esta configuración se hace una sola vez y aplica a todos tus proyectos.

### Crear una cuenta en GitHub

Ve a https://github.com y crea una cuenta gratuita. El correo que uses aquí no tiene que ser el mismo que configuraste en Git, pero es recomendable que coincidan.

---

## 3. Crear un Repositorio

Un repositorio es el punto de partida de cualquier proyecto en GitHub.

### Desde GitHub (recomendado para empezar)

1. Inicia sesión en GitHub
2. Haz clic en el botón **New** en la esquina superior izquierda
3. Escribe un nombre para el repositorio (sin espacios, usa guiones si necesitas separar palabras)
4. Elige si será **Public** (cualquiera puede verlo) o **Private** (solo tú y quienes invites)
5. Marca la opción **Add a README file** para que el repositorio no quede vacío
6. Haz clic en **Create repository**

### Desde tu computadora

Si ya tienes una carpeta con archivos y quieres convertirla en un repositorio:

```bash
cd ruta/de/tu/carpeta
git init
```

El comando `git init` crea una carpeta oculta llamada `.git` donde Git guarda todo el historial. No debes modificar esa carpeta manualmente.

---

## 4. Clonar un Repositorio

Clonar significa descargar un repositorio de GitHub a tu computadora para trabajar en él.

```bash
git clone https://github.com/usuario/nombre-del-repositorio.git
```

Esto crea una carpeta en tu computadora con todos los archivos del proyecto y el historial completo. La URL la encuentras en el repositorio de GitHub, en el botón verde que dice **Code**.

---

## 5. El Flujo de Trabajo Diario

Este es el ciclo que repetirás cada vez que trabajes en un proyecto.

### Paso 1: Revisar el estado actual

Antes de hacer cualquier cosa, es útil saber qué archivos han cambiado:

```bash
git status
```

Este comando muestra qué archivos fueron modificados, cuáles son nuevos y cuáles están listos para el próximo commit.

### Paso 2: Preparar los cambios

Cuando terminas de modificar archivos y quieres guardarlos en un commit, primero debes indicarle a Git cuáles incluir. A esto se le llama agregar al staging area:

```bash
# Agregar un archivo específico
git add nombre-del-archivo.txt

# Agregar todos los archivos modificados de una vez
git add .
```

El staging area es como un borrador: puedes agregar y quitar archivos antes de hacer el commit definitivo.

### Paso 3: Hacer un commit

Una vez que tienes los archivos preparados, confirmas los cambios con un mensaje que describa qué hiciste:

```bash
git commit -m "Agrega la función de inicio de sesión"
```

El mensaje debe ser claro y describir el cambio, no el archivo. En lugar de "modifica login.js", escribe "corrige el error de validación en el formulario de login".

### Paso 4: Subir los cambios a GitHub

Para que tus commits queden guardados en GitHub (y no solo en tu computadora):

```bash
git push origin main
```

`origin` es el nombre que Git le da al repositorio remoto (el que está en GitHub) y `main` es el nombre de la rama.

### Paso 5: Traer cambios de GitHub

Si alguien más subió cambios al repositorio, debes descargarlos antes de seguir trabajando:

```bash
git pull origin main
```

---

## 6. Trabajar con Ramas

Las ramas permiten trabajar en algo nuevo sin tocar el código principal que ya funciona. La rama `main` debe contener siempre una versión estable del proyecto.

### Crear una rama nueva

```bash
git checkout -b nombre-de-la-rama
```

Esto crea la rama y te mueve a ella al mismo tiempo. Usa nombres descriptivos como `nueva-pagina-contacto` o `correccion-error-login`.

### Ver en qué rama estás

```bash
git branch
```

La rama activa aparece marcada con un asterisco.

### Cambiar de rama

```bash
git checkout nombre-de-la-rama
```

### Subir una rama a GitHub

```bash
git push origin nombre-de-la-rama
```

### Fusionar una rama con main

Cuando terminas el trabajo en tu rama y quieres incorporarlo al proyecto principal:

```bash
git checkout main
git merge nombre-de-la-rama
```

### Eliminar una rama después de fusionarla

```bash
git branch -d nombre-de-la-rama
```

---

## 7. Pull Requests

Un pull request es la forma estándar de proponer cambios en un proyecto colaborativo. En lugar de fusionar directamente, propones la fusión para que alguien más revise el código primero.

### Crear un pull request

1. Sube tu rama a GitHub con `git push origin nombre-de-la-rama`
2. Ve al repositorio en GitHub
3. GitHub mostrará un aviso con tu rama y un botón **Compare & pull request**. Haz clic en él
4. Escribe un título y una descripción explicando qué cambios hiciste y por qué
5. Haz clic en **Create pull request**

### Revisar un pull request

En la pestaña **Files changed** puedes ver exactamente qué líneas se agregaron (en verde) y cuáles se eliminaron (en rojo). Puedes dejar comentarios en líneas específicas.

Cuando todo está correcto, se hace clic en **Merge pull request** para fusionar los cambios con `main`.

---

## 8. El archivo .gitignore

Algunos archivos no deben subirse a GitHub: contraseñas, configuraciones locales, carpetas de dependencias pesadas, etc. El archivo `.gitignore` le indica a Git cuáles ignorar.

Se crea en la carpeta raíz del proyecto con el nombre `.gitignore` y cada línea es un patrón de archivos o carpetas a excluir:

```
# Carpeta de dependencias de Node.js
node_modules/

# Archivo de variables de entorno (puede contener contraseñas)
.env

# Archivos generados automáticamente
dist/
build/
*.log

# Archivos del sistema operativo
.DS_Store
Thumbs.db
```

Git ignorará todo lo que coincida con estos patrones y nunca lo incluirá en un commit.

---

## 9. Comandos de Referencia Rápida

```bash
# Ver el historial de commits
git log --oneline

# Ver qué cambió en los archivos antes de hacer commit
git diff

# Deshacer cambios en un archivo antes del commit
git checkout -- nombre-del-archivo.txt

# Guardar cambios temporalmente sin hacer commit (útil para cambiar de rama)
git stash

# Recuperar los cambios guardados con stash
git stash pop

# Revertir el último commit sin perder los cambios
git reset --soft HEAD~1
```

---

## 10. Buenas Practicas

- Haz commits frecuentes y pequeños. Es mejor muchos commits descriptivos que uno grande con semanas de trabajo.
- El mensaje del commit debe explicar el "qué" y el "por qué", no el "cómo".
- Nunca subas información sensible como contraseñas o tokens de acceso. Una vez en GitHub, aunque borres el archivo, queda en el historial.
- Antes de empezar a trabajar, haz siempre `git pull` para asegurarte de tener la versión más reciente.
- Usa ramas para cualquier cambio que no sea trivial. Trabajar directamente en `main` es una práctica que puede causar problemas en proyectos colaborativos.

---

## Recursos para Continuar

- Documentacion oficial de Git: https://git-scm.com/doc
- Guias de GitHub en español: https://docs.github.com/es
- Practica interactiva de ramas: https://learngitbranching.js.org/?locale=es_ES
- Curso gratuito de GitHub Skills: https://skills.github.com
