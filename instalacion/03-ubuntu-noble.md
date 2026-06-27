# 03 — Ubuntu Noble

## Instalar Ubuntu Noble desde Hekate

1. Desde Hekate ir a **Tools → Install Linux**
2. Seleccionar los archivos `l4t.00` / `l4t.01` desde `switchroot/install/`
3. Iniciar la instalación y esperar (puede tardar varios minutos)

## Primer arranque

1. En Hekate seleccionar la entrada de Ubuntu Noble
2. El sistema arrancará en Ubuntu — el primer arranque puede tardar más de lo normal
3. Completar la configuración inicial del sistema (usuario, contraseña, etc.)

## Verificar la instalación

```bash
uname -a        # Verificar kernel ARM64
lsb_release -a  # Verificar Ubuntu Noble 24.04
df -h           # Verificar particiones
```

## Activar repositorios universe y multiverse

Necesario para instalar la mayoría de herramientas:

```bash
sudo add-apt-repository universe
sudo add-apt-repository multiverse
sudo apt update
```

> ℹ️ En Ubuntu Noble ARM64 muchos paquetes solo están disponibles si universe y multiverse están activados.
