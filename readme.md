# Guía de Resolución: Ejercicio Git Colegio

### 1. Configuración de Identidad
```bash
git config --global user.name "Carlos201120"
git config user.name # Verificación
```

### 2 y 3. Clonar en carpeta específica (Paso único)
```bash
git clone https://github.com/Carlosrt15/Colegio colegio_Carlos
cd colegio_Carlos
```

### 4 y 5. Crear archivo profesores y subir al remoto
```bash
touch profesores.txt
git add profesores.txt
git commit -m "Añadido archivo profesores.txt"
git push origin main
```

### 6. Enlace al repositorio secundario
```bash
git remote add copiaColegio https://github.com
```

### 8. Comprobar cambios (Solo inspección)
```bash
git fetch origin
git status # Aquí verás que el remoto va por delante
```

### 9. Actualizar localmente
```bash
git pull origin main
```

### 10. Provocar y Resolver Conflicto
*Modifica alumnos.txt en la web, luego modifícalo localmente y ejecuta:*

```bash
# 1. Intentar subir (Dará error)
git push origin main

# 2. Traer cambios para generar el conflicto
git pull origin main

# 3. Resolver (Editar el archivo manualmente con nano o VS Code)
nano alumnos.txt

# 4. Confirmar resolución y subir
git add alumnos.txt
git commit -m "Conflicto resuelto en alumnos.txt"
git push origin main
```
