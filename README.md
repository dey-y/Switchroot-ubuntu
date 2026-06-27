# Nintendo Switch — Ubuntu Noble 24.04 ARM64

Documentación del proceso de instalación y configuración de Ubuntu Noble 24.04.4 LTS ARM64 en una Nintendo Switch V1 (unpatched) mediante Switchroot.

## ¿De qué trata este proyecto?

Instalación de Linux nativo en una Nintendo Switch V1 (2017–2018, chipset Tegra X1 sin parchear) usando el proyecto [Switchroot](https://wiki.switchroot.org/), con el objetivo de disponer de un sistema Linux ARM64 completamente funcional en hardware portátil.

## ¿Para qué sirve?

- Tener un sistema Linux completo y portátil
- Aprender administración de sistemas en ARM64
- Usar herramientas de red, desarrollo y scripting en cualquier lugar
- Base para proyectos de ciberseguridad, desarrollo o aprendizaje

## Requisitos previos

| Componente | Detalle |
|---|---|
| Dispositivo | Nintendo Switch V1 (serial XAW o XAJ pre-2018) |
| Condición | Unpatched (vulnerable a exploit Fusée Gelée) |
| microSD | 64GB mínimo recomendado |
| PC | Windows/Linux para inyectar payload RCM |
| Software | TegraRcmGUI, Hekate, Switchroot Ubuntu Noble |

## Cómo verificar si tu Switch es compatible

El número de serie debe empezar por `XAW1`, `XAW4`, `XAW7` o `XAJ7` y la fecha de fabricación debe ser anterior a julio de 2018. Puedes verificarlo en [ismyswitchpatched.com](https://ismyswitchpatched.com).

## Estructura

- [Instalación](./instalacion/)
  - [01 — Preparación de la microSD](./instalacion/01-preparacion-sd.md)
  - [02 — RCM y Hekate](./instalacion/02-rcm-hekate.md)
  - [03 — Ubuntu Noble](./instalacion/03-ubuntu-noble.md)
- [Configuración](./configuracion/)
  - [Hekate](./configuracion/hekate.md)
  - [SSH](./configuracion/ssh.md)
  - [Herramientas](./configuracion/herramientas.md)
- [Problemas frecuentes](./problemas/soluciones.md)

## Estado actual

- ✅ Ubuntu Noble 24.04.4 LTS ARM64 instalado y funcionando
- ✅ Hekate v6.5.3 + Nyx configurado con autoboot
- ✅ microSD 64GB particionada (HOS FAT32 ~9GB + Linux EXT4 ~49GB)
- ✅ SSH configurado y operativo
