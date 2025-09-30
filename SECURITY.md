# Seguridad y Accesibilidad en el Repositorio

## Exclusión de archivos sensibles
- Se utiliza `.gitignore` para evitar subir:
  - Archivos de configuración local (`.env`, `.local`).
  - Dependencias externas (`node_modules/`).
  - Archivos temporales o del sistema (`.DS_Store`, `Thumbs.db`).

## Control de acceso en GitHub
- **Lectura (Read):** Para usuarios que solo deben consultar el código.
- **Escritura (Write):** Para colaboradores que pueden añadir y modificar código.
- **Administrador (Admin):** Solo para responsables del proyecto (gestión de ramas, permisos y configuración).

## Buenas prácticas de seguridad
- Uso de **ramas protegidas** (ej. `main`) para evitar cambios directos sin revisión.
- Uso de **pull requests** para que el código pase revisión antes de integrarse.
- **Revisión de cambios** por al menos un colaborador antes de mezclar.
- Configuración de **copias de seguridad** del repositorio en la nube (GitHub ya las garantiza).

## Recuperación del repositorio
- En caso de error o pérdida de datos, se pueden recuperar commits anteriores desde el historial de Git.
- Los colaboradores pueden clonar el repositorio en cualquier momento para mantener copias locales.

## Resultados de las pruebas de permisos

- **Read:** El usuario solo pudo ver el repositorio, sin posibilidad de modificar nada.  
- **Write:** El usuario pudo subir cambios al repositorio, crear ramas y hacer commits.  
- **Admin:** El usuario tuvo acceso completo (incluyendo gestión de permisos y configuración).  

### Conclusión
El rol más adecuado para un colaborador en un equipo de desarrollo es **Write**, mientras que el rol de **Admin** debe reservarse solo al responsable del proyecto.
