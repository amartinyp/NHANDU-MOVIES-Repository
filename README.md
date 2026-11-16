# NHANDU MOVIES · Jellyfin Smart Labels

Repositorio público de distribución del complemento **NHANDU MOVIES / Jellyfin Smart Labels** para Jellyfin Server 12.2.x.

## Estado

**Primera versión de pruebas publicada: 0.2.0.0.**

- Release: https://github.com/amartinyp/NHANDU-MOVIES-Repository/releases/tag/v0.2.0.0
- Paquete: `NHANDU-MOVIES-0.2.0.0.zip`
- Manifiesto del repositorio: https://raw.githubusercontent.com/amartinyp/NHANDU-MOVIES-Repository/main/manifest.json

## Compatibilidad prevista

- Jellyfin Server 12.2.0
- Linux x64 / Docker
- Jellyfin Web para la administración y el catálogo propio

No se declara compatibilidad con Android, Android TV, iOS, televisores ni clientes de terceros hasta realizar pruebas específicas.

## Dependencias opcionales de integración web

El complemento puede cargarse sin estos complementos adicionales. Para activar la experiencia web completa se necesitan versiones compatibles con Jellyfin 12.2.0 de:

- **File Transformation**: necesario para inyectar el cliente web, servir las rutas virtuales del catálogo y habilitar los carteles.
- **Plugin Pages**: necesario para añadir NHANDU MOVIES al menú habitual de usuario.

Sin estas dependencias, la página de administración del complemento seguirá disponible, pero las integraciones visuales y el acceso de usuario al catálogo no estarán activos. Jellyfin no instala automáticamente estas dependencias al instalar NHANDU MOVIES desde un repositorio.

## Instalación

1. En Jellyfin, abre **Panel de control → Complementos → Repositorios**.
2. Añade esta dirección:
   `https://raw.githubusercontent.com/amartinyp/NHANDU-MOVIES-Repository/main/manifest.json`
3. Guarda el repositorio y consulta el catálogo de complementos.
4. Antes de instalar en el servidor principal, realiza una copia de seguridad de la configuración y confirma que las dependencias opcionales están resueltas si quieres la experiencia web completa.

La publicación actual es una versión de pruebas. No instales todavía el complemento en el servidor principal: primero debemos cerrar y probar el procedimiento de instalación y reversión para tu entorno Docker/Portainer.

## Privacidad del proyecto

Este repositorio contiene únicamente material público de distribución y documentación. El código fuente permanece en el repositorio privado de desarrollo.

## Aviso

Un complemento se ejecuta dentro del proceso de Jellyfin. Haz siempre una copia de seguridad de la configuración antes de instalarlo y conserva un procedimiento de reversión.
