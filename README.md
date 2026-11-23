# Promeia Music

Promeia Music es una aplicación Android de reproducción y gestión de música local, desarrollada desde cero con Kotlin y Jetpack Compose.

> **Proyecto greenfield:** Phoenix Music se considera únicamente una referencia de requisitos funcionales. No se copian ni importan sus archivos, código, recursos ni estructura interna.

## Objetivos funcionales

- Reproducir archivos de audio locales.
- Explorar la biblioteca por canciones, álbumes y artistas.
- Crear, renombrar y eliminar playlists; agregar y quitar canciones.
- Mostrar una acción única **Agregar a playlist** que abre un selector de playlists.
- Buscar carátulas en servicios web y permitir guardarlas localmente junto a la biblioteca.
- Editar metadatos y asignar, cambiar o quitar carátulas.
- Importar listas de Spotify usando únicamente integraciones oficiales y metadatos permitidos; no descargar audio protegido.
- Mantener una interfaz original con identidad visual propia de Promeia Music.

## Almacenamiento

Cuando los permisos y las APIs de Android lo permitan, los archivos administrados por la app se organizarán así:

```text
Music/Promeia Music/
├── Music/
└── Image/
```

La app respetará el almacenamiento con alcance de Android (Scoped Storage), los permisos vigentes y las decisiones del usuario. No moverá archivos personales sin autorización.

## Arquitectura propuesta

- **Lenguaje/UI:** Kotlin + Jetpack Compose + Material 3.
- **Reproducción:** AndroidX Media3 / ExoPlayer.
- **Datos:** Room para playlists, referencias de biblioteca y metadatos propios.
- **Acceso multimedia:** MediaStore y Storage Access Framework.
- **Preferencias:** DataStore.
- **Imágenes:** capa de búsqueda/descarga desacoplada, con proveedor configurable y caché local.
- **Spotify:** OAuth y Web API oficial para metadatos/listas, sujeto a disponibilidad, permisos y políticas de Spotify.

## Etapas de desarrollo

1. Especificación y arquitectura base.
2. Esqueleto Android compilable y configuración Gradle.
3. Biblioteca local y reproducción.
4. Playlists y selector «Agregar a playlist».
5. Metadatos, carátulas y organización de archivos.
6. Integración oficial de Spotify.
7. Pruebas, accesibilidad, pulido visual y generación de APK.

## Estado

En desarrollo. Cada etapa se marcará como completada solo después de verificar sus archivos o pruebas correspondientes.
