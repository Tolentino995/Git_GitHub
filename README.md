
# Curso de Git_GitHub 

## Comandos

### Configuraciones Globales

**git config** --global [user.name](http://user.name/) "nombre"

**git config** --global [user.email](http://user.email/) "correo"

**git config**  --global alias."nombre del alias que queremos nosotros"

"comando(ejemplo: git log --graph --decorate --all --oneline )"

---

**cd** "nombre donde me quiero desplazar"

**cd ..** (para atras)

**ls** (listado de carpeta donde me encuentro)

**touch** (para crear un archivo)

**git init** (para instanciarme)

**git add + tab** y seleccionar lo que quiero añadir a mi commit (añadir elemento para hacer mi commit)

**git status** (para ver el estado de mi carpeta)

**git commit -m** "nombre que le quiero dar a mi commit" (hacer una versión de mi carpeta)

**git checkout** "nombre del archivo para volver a su ultimo commit (poder desplazarnos)"

“Tambien puede desaser cambios”

**git reset** —hard “similiar a checkout pero con la diferecia de eliminar los de adelante”

**git diff** (para ver las modificaciones antes de que hagamos un commit)

**git tag** “El nombre que queramos para poder identificarlo” (nos podemos desplazar con el checkout y el nombre del tag)

**git branch** (nombre de la rama) “Crear una nueva rama”

**git branch** “para consultar las ramas”

**git branch** -d (nombre de la rama) “para eliminar la rama”

**git switch** (nombre de la rama) “Para desplazarme en cada rama”

**git merge** (nombre de la rama) “Adjuntar o unir”

**git stash** “Comit pero temporal”

**git stash list** “lista de comit temporal”

**git stash pop** “Se usa para recuperar los elemento que guardamos temporalmente”

**git stash dop** “Se usa para eliminar los elemento que guardamos temporalmente”

**git reflog** “Para ver todo lo que hemos realizado”

---

## GitHub

Nos creamos una cuenta, un repositorio propio donde lo tenemos que ir armando como si fuera un muero de facebook. Ahora generamos una conexión con SSH

**git remote add origin** “mas el link del repositorio para enlazar el repositorio con el ordenador”

**git push -u origin main**  “para subir los archivos desde ordenaro al repositorio ”

git fetch 
