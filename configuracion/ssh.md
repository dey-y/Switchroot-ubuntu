# SSH

## Instalar OpenSSH Server

```bash
sudo systemctl stop packagekit
sudo apt install openssh-server -y
```

## Verificar que SSH está activo

```bash
sudo systemctl status ssh
```

## Conectarse a la Switch por SSH

Desde otro dispositivo en la misma red:

```bash
ssh usuario@192.168.1.140
```

> ℹ️ La IP de la Switch en la red local es `192.168.1.140`. Si cambia, verificar con `ip a` desde la Switch.

## Activar SSH al arranque

```bash
sudo systemctl enable ssh
```
