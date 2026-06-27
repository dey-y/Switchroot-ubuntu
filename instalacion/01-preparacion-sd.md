# 01 — Preparación de la microSD

## Materiales necesarios

- microSD 64GB o superior
- PC con Windows o Linux
- Lector de tarjetas SD

## Descargas necesarias

| Archivo | Fuente |
|---|---|
| Hekate + Nyx | [github.com/CTCaer/hekate](https://github.com/CTCaer/hekate/releases) |
| Ubuntu Noble (Switchroot) | [wiki.switchroot.org](https://wiki.switchroot.org/wiki/linux/l4t-ubuntu-noble-installation-guide) |
| TegraRcmGUI | [github.com/eliboa/TegraRcmGUI](https://github.com/eliboa/TegraRcmGUI/releases) |

## Pasos

1. Formatear la microSD en FAT32 desde el PC
2. Copiar los archivos de Hekate a la raíz de la microSD:
   - `hekate_ctcaer_x.x.x.bin`
   - Carpeta `bootloader/`
3. Crear la carpeta `switchroot/install/` en la microSD
4. Colocar los archivos `l4t.00` y `l4t.01` dentro de `switchroot/install/`

> ⚠️ Los archivos `l4t.00` y `l4t.01` deben estar exactamente en `switchroot/install/` — ruta crítica, si no están ahí la instalación no los encontrará.
