# 🚀 Curso de Git & GitHub  

## 📌 Comandos esenciales  

### 🔧 Configuraciones Globales  

```bash
git config --global user.name "Tu Nombre"  # Configurar nombre de usuario
git config --global user.email "tuemail@example.com"  # Configurar correo electrónico
git config --global alias.[nombre_alias] "[comando]"  # Crear un alias personalizado
```
📌 *Ejemplo de alias útil:*  
```bash
git config --global alias.hist "log --graph --decorate --all --oneline"
```

---

## 🖥️ Comandos básicos de Git  

### 📂 Navegación en la terminal  

```bash
cd "nombre_carpeta"     # Entrar a una carpeta  
cd ..                   # Ir a la carpeta anterior  
ls                      # Listar archivos y carpetas  
touch archivo.txt       # Crear un archivo vacío  
```
## 🔐 Configuración de SSH en GitHub  

1️⃣ Verificar si ya tenés claves SSH  
```bash
ls -al ~/.ssh           # Listar claves existentes en la carpeta .ssh  
```
---
2️⃣ Generar una nueva clave SSH  
```bash
ssh-keygen -t ed25519 -C "tu-email@ejemplo.com"
```
- Cuando te pregunte la ruta, presioná **Enter** para aceptar la ubicación por defecto (`~/.ssh/id_ed25519`).  
- Si querés, podés ponerle una **passphrase** para más seguridad (opcional).  
---
3️⃣ Activar el **agente SSH**  
```bash
eval "$(ssh-agent -s)"   # Iniciar el agente SSH en segundo plano  
ssh-add ~/.ssh/id_ed25519   # Agregar tu clave privada al agente  
```
4️⃣ Copiar tu **clave pública**  
```bash
clip < ~/.ssh/id_ed25519.pub   # Copiar clave pública en Windows  
# En Linux/macOS sería:
cat ~/.ssh/id_ed25519.pub
```
- Pega el contenido en **GitHub → Settings → SSH and GPG keys → New SSH key**.  
---
5️⃣ Probar la conexión con GitHub  
```bash
ssh -T git@github.com
```
- Si todo está bien, te dirá:  
  `Hi <tu-usuario>! You've successfully authenticated, but GitHub does not provide shell access.`  

### 🔨 Iniciar y trabajar con Git  

```bash
git init                # Inicializar un repositorio Git  
git status              # Ver el estado de los archivos  
git add archivo.txt     # Agregar un archivo al staging  
git add .               # Agregar todos los archivos  
git commit -m "Mensaje del commit"  # Guardar cambios con un mensaje  
```

📌 *Ejemplo:*  
```bash
git add index.html
git commit -m "Añadí la estructura HTML inicial"
```

### 🔄 Revertir cambios  

```bash
git checkout archivo.txt   # Revertir cambios de un archivo a la última versión confirmada  
git reset --hard           # Eliminar todos los cambios no confirmados  
git diff                   # Ver diferencias antes de hacer commit  
```

### 🏷️ Trabajando con tags  

```bash
git tag v1.0               # Crear una etiqueta (versión)  
git checkout v1.0          # Moverse a un tag específico  
```

---

## 🌿 Trabajando con ramas  

```bash
git branch                # Ver todas las ramas  
git branch nueva-rama     # Crear una nueva rama  
git switch nueva-rama     # Cambiar a otra rama  
git branch -d nueva-rama  # Eliminar una rama  
git merge nombre-rama     # Unir ramas  
```

📌 *Ejemplo:*  
```bash
git branch feature-login
git switch feature-login
```

---

## 📌 Guardado temporal con Stash  

```bash
git stash                 # Guardar cambios temporalmente  
git stash list            # Ver los cambios guardados  
git stash pop             # Restaurar el último stash  
git stash drop            # Eliminar un stash  
```

---

## 🔍 Historial y recuperación  

```bash
git reflog                # Ver todas las acciones realizadas  
```

---

## 🌎 Comandos para GitHub  

```bash
git remote add origin "URL-del-repo"  # Conectar repositorio local con GitHub  
git push -u origin main               # Subir cambios a GitHub  
git fetch                              # Obtener cambios remotos sin fusionarlos  
git pull                               # Obtener y fusionar cambios remotos  
git clone URL                          # Clonar un repositorio  
git push                               # Subir cambios al repositorio  
```

📌 *Ejemplo:*  
```bash
git remote add origin https://github.com/usuario/repo.git
git push -u origin main
```

---

## 🏆  GitHub Comunidad (No son comandos)  

- **🔀 Fork** → Clonar un repositorio de otro usuario sin permisos de edición.  
- **🔄 Sync Fork** → Mantener sincronizado tu Fork con el repositorio original.  
- **🤝 Contribute** → Proponer cambios a otro repositorio mediante un *Pull Request*.  

---

### ✨ Ejemplo de código bien estructurado  

```bash
# 🔀 Crear y cambiar a una nueva rama
git branch feature-login  
git switch feature-login  

# 📌 Agregar cambios al área de staging
git add index.html  

# 💾 Confirmar cambios con un mensaje descriptivo
git commit -m "Añadí la estructura HTML inicial"  

# 🚀 Subir los cambios al repositorio remoto
git push origin feature-login  
```

---
