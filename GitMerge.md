# 🧩 **Guía Completa para Realizar un Merge en Git**

## 📘 **¿Qué es un Merge en Git?**
La fusión (*merge*) en Git es el proceso que permite unir dos ramas con historiales de desarrollo independientes. Usando el comando `git merge`, se integran los cambios de una rama en otra, generando un nuevo commit de fusión que combina el historial de ambas ramas. 

El merge se realiza desde la **rama actual**, mientras que la rama que se desea fusionar permanece sin cambios. Esto permite mantener un control claro del historial.

---

## 🔧 **¿Cómo funciona Git Merge?**
El proceso de fusión combina las secuencias de confirmaciones (commits) de dos ramas. Para ello, Git:
1. **Busca una confirmación base común** (punto de divergencia de las ramas).  
2. **Fusiona los cambios** realizados en ambas ramas desde esa base.  
3. **Crea un nuevo commit de fusión** para reflejar el estado final.  

Si no hay cambios en conflicto, la fusión se realiza automáticamente. En caso de conflicto, Git te pedirá resolver manualmente las diferencias antes de continuar.  

---

## 📚 **Pasos para unir dos ramas en Git**

### 🔹 **1. Cambiar a la rama de destino**
Primero, asegúrate de estar en la rama donde deseas integrar los cambios. Para ello, utiliza el comando:  
```bash
git checkout <nombre-de-la-rama-destino>
```

Por lo general, esta será la rama principal, como main o master.
🔹 2. Fusionar la rama deseada en la rama actual

Para fusionar otra rama, usa el comando:

```bash
git merge <nombre-de-la-rama-origen>
```

Esto combinará los cambios de la rama de origen en la rama actual.
🔹 3. Resolver conflictos (si los hay)

Si hay conflictos, Git te notificará los archivos afectados. Deberás editar los archivos manualmente, eliminando las secciones de conflicto y eligiendo los cambios que deseas conservar. Una vez resueltos, sigue estos pasos:

```bash
git add <archivos-con-conflicto>
git commit
```

El comando git add marca los archivos como resueltos, y git commit finaliza la fusión.
📋 Comandos clave de Git Merge
Comando	Descripción
- **git checkout <rama>**	Cambia a la rama donde quieres fusionar.
- **git merge <rama>**	Fusiona la rama especificada en la actual.
- **git branch -d <rama>**	Elimina una rama que ya no se necesita.
- **git fetch**	Actualiza la información de ramas remotas.
- **git pull**	Descarga y fusiona cambios del remoto.
- **git push**	Sube los cambios locales al repositorio remoto.

#### 📦 Ejemplo práctico

Supongamos que estás en la rama master y quieres fusionar los cambios de la rama feature/cabecera. Los pasos son:

# 1. Cambia a la rama master
```bash
git checkout master
```

# 2. Fusiona la rama feature/cabecera con master
```bash
git merge feature/cabecera
```
Si no hay conflictos, la fusión se completará automáticamente. Si hay conflictos, deberás resolverlos manualmente.

#### ⚠️ Consejos importantes

- **Guarda tu trabajo antes de cambiar de rama**: Usa git add y git commit para evitar la pérdida de cambios no guardados.
- **Resuelve conflictos con paciencia**: Si hay conflictos, edita los archivos y marca los conflictos como resueltos.
- **Elimina ramas obsoletas**: Usa **git branch -d <rama>** para limpiar ramas que ya no necesites.
- **Mantén tu repositorio actualizado**: Usa git fetch y git pull para asegurarte de tener los cambios más recientes antes de hacer un merge.

### 🚀 Conclusión

El merge en Git te permite combinar ramas y unificar el historial de cambios. Siguiendo los pasos de esta guía, podrás hacerlo de forma segura y eficiente, evitando conflictos o solucionándolos si se presentan. ¡Ahora estás listo para dominar Git Merge como un experto! 🚀