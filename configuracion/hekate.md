# Configuración de Hekate

## Versión utilizada

Hekate v6.5.3 + Nyx

## Configurar autoboot

Para que la Switch arranque directamente en Ubuntu Noble sin pasar por el menú de Hekate cada vez:

1. En Hekate ir a **Config → Bootloader**
2. Seleccionar la entrada de Ubuntu Noble
3. Activar **Autoboot**

Con autoboot activo, al inyectar el payload la Switch arranca directamente en Linux.

## Entradas de arranque

Hekate permite tener varias entradas configuradas:

- **Ubuntu Noble** — Linux ARM64 (entrada principal)
- **HOS** — Sistema original de Nintendo (para acceder a la Switch normal si es necesario)

## Notas

- La configuración de Hekate se guarda en `bootloader/hekate_ipl.ini` en la microSD
- Nyx es la interfaz gráfica de Hekate — permite navegar con la pantalla táctil de la Switch
