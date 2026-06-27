# Problemas frecuentes

## apt no funciona / se queda bloqueado

**Causa:** PackageKit bloquea apt en Ubuntu Noble.

**Solución:** Detener PackageKit antes de cualquier operación con apt:

```bash
sudo systemctl stop packagekit
sudo apt install <paquete>
```

## Archivos l4t no encontrados durante la instalación

**Causa:** Los archivos `l4t.00` y `l4t.01` no están en la ruta correcta.

**Solución:** Verificar que estén exactamente en `switchroot/install/` dentro de la microSD. No vale ponerlos en la raíz ni en otra subcarpeta.

## La Switch vuelve al sistema de Nintendo al apagarse

**Causa:** El payload de Hekate no es persistente. Al apagar completamente la Switch se pierde y arranca el sistema original de Nintendo (HOS).

**Solución:** Usar siempre **suspender** en lugar de apagar. Si se apaga por completo, hay que volver a entrar en RCM e inyectar el payload con TegraRcmGUI desde el PC.

## Paquete no disponible para ARM64

**Causa:** Los repositorios universe y multiverse no están activados, o el paquete directamente no tiene build ARM64.

**Solución:**
```bash
sudo add-apt-repository universe
sudo add-apt-repository multiverse
sudo apt update
```

Si el paquete sigue sin aparecer, buscar método alternativo de instalación (git clone, curl installer, etc.). Parrot OS no tiene build ARM64 — Ubuntu Noble con herramientas encima es el enfoque correcto.

## Switch no entra en modo RCM

**Causa:** Switch parcheada, RCM jig mal insertado, o pines no cortocircuitados correctamente.

**Solución:** Verificar número de serie en [ismyswitchpatched.com](https://ismyswitchpatched.com). Si la Switch es compatible, revisar que el jig esté bien insertado en el rail derecho del Joy-Con antes de pulsar Vol+ + Power.
