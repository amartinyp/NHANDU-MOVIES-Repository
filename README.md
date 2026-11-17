# NHANDU MOVIES · Jellyfin Smart Labels

Repositorio público de distribución del complemento **NHANDU MOVIES / Jellyfin Smart Labels** para Jellyfin Server 12.2.x.

## Estado

**Versión estable publicada: 1.0.5.0.**

- Tag: https://github.com/amartinyp/NHANDU-MOVIES-Repository/tree/v1.0.5.0
- Paquete Jellyfin directo: `NHANDU-MOVIES-1.0.5.0.zip`
- Bundle manual separado: `NHANDU-MOVIES-1.0.5.0-manual-installer.zip` (generado por CI)
- Manifiesto del repositorio: https://raw.githubusercontent.com/amartinyp/NHANDU-MOVIES-Repository/main/manifest.json

## Compatibilidad prevista

- Jellyfin Server 12.2.0
- Linux x64 / Docker
- Jellyfin Web para la administración, catálogo propio y carteles promocionales dentro del catálogo.

No se declara compatibilidad con Android, Android TV, iOS, televisores ni clientes de terceros hasta realizar pruebas específicas.

## Complementos necesarios

Este repositorio incluye tres entradas en el catálogo para que puedas encontrarlos desde una sola dirección:

| Complemento | Versión Jellyfin 12.2 | Función |
|---|---:|---|
| File Transformation | 3.0.3.0 | Permite integrar transformaciones en Jellyfin Web sin modificar los archivos originales del cliente. |
| Plugin Pages | 3.0.3.0 | Permite añadir NHANDU MOVIES al menú de usuario. Necesita File Transformation. |
| NHANDU MOVIES | 1.0.5.0 | Administración de etiquetas y catálogo NHANDU MOVIES. |

Los dos primeros son complementos de terceros desarrollados por **IAmParadox27**. Sus paquetes se descargan directamente de sus publicaciones originales de GitHub; este repositorio no vuelve a empaquetarlos ni modifica sus binarios.

**Importante:** Jellyfin no instala automáticamente las dependencias declaradas por otros complementos. Por eso debes instalar los tres desde el catálogo, en este orden:

1. File Transformation.
2. Plugin Pages.
3. NHANDU MOVIES.

Puedes instalar los tres antes de reiniciar Jellyfin. Cuando los tres aparezcan como instalados y Jellyfin solicite reinicio, reinicia el servidor una sola vez desde Portainer.

## Instalación desde Jellyfin

1. Abre **Panel de control → Complementos → Repositorios**.
2. Añade esta dirección:
   `https://raw.githubusercontent.com/amartinyp/NHANDU-MOVIES-Repository/main/manifest.json`
3. Guarda el repositorio y abre el catálogo.
4. Instala los tres complementos siguiendo el orden anterior.
5. Reinicia Jellyfin una vez, cuando hayas terminado las tres instalaciones.

La publicación 1.0.0.0 es una primera versión estable preparada para pruebas controladas. Antes de instalar en el servidor principal, realiza una copia de seguridad de la configuración. No cambies la imagen Docker, los volúmenes ni los archivos multimedia.

## Qué modifica NHANDU MOVIES

- Guarda las etiquetas y asignaciones en la configuración propia del complemento.
- Dibuja las etiquetas sobre las carátulas dentro del catálogo NHANDU MOVIES.
- Ordena por año de estreno descendente y, en caso de empate, por título alfabético.
- No modifica los archivos multimedia, las imágenes originales ni los metadatos de Jellyfin.

La ordenación por año afecta únicamente al catálogo NHANDU MOVIES, no a todas las pantallas nativas de Jellyfin.

## Privacidad y atribuciones

El código fuente de NHANDU MOVIES permanece en el repositorio privado de desarrollo. Los complementos File Transformation y Plugin Pages mantienen sus propias licencias y autoría; sus binarios se descargan desde los repositorios originales:

- https://github.com/IAmParadox27/jellyfin-plugin-file-transformation
- https://github.com/IAmParadox27/jellyfin-plugin-pages

## Aviso de seguridad

Un complemento se ejecuta dentro del proceso de Jellyfin. Haz siempre una copia de seguridad de la configuración antes de instalarlo y conserva un procedimiento de reversión. No instales esta versión de pruebas en el servidor principal hasta que hayas revisado el plan de instalación y copia de seguridad.
