# 02 — RCM y Hekate

## ¿Qué es el modo RCM?

RCM (Recovery Mode) es un modo de arranque del chipset Tegra X1 que permite inyectar payloads sin restricciones. Las Switch V1 sin parchear son vulnerables al exploit Fusée Gelée, que aprovecha este modo para cargar software no oficial como Hekate.

## Materiales necesarios

- RCM jig (~2€ en AliExpress) — recomendado para uso recurrente
- Cable USB-C
- PC con TegraRcmGUI instalado

> ℹ️ El RCM jig se puede sustituir cortocircuitando manualmente los pines 1 y 10 del rail derecho del Joy-Con, pero el jig es mucho más cómodo si vas a entrar en RCM frecuentemente.

## Entrar en modo RCM

1. Apagar la Switch completamente
2. Insertar el RCM jig en el rail derecho del Joy-Con
3. Mantener pulsado **Vol+** y pulsar **Power**
4. La pantalla quedará en negro — correcto, la Switch está en modo RCM

## Inyectar el payload con TegraRcmGUI

1. Conectar la Switch al PC mediante USB-C
2. Abrir **TegraRcmGUI v2.6**
3. Seleccionar `hekate_ctcaer_x.x.x.bin` como payload
4. Pulsar **Inject payload**
5. Hekate arrancará en la Switch

## Particionar la microSD desde Hekate

Una vez en Hekate:

1. Ir a **Tools → Partition SD Card**
2. Asignar espacio:
   - HOS FAT32: ~9GB (sistema Nintendo)
   - Linux EXT4: resto (~49GB en una microSD de 64GB)
3. Confirmar y esperar a que termine el proceso

## ⚠️ Suspender vs apagar la Switch

La Switch con Linux **no se debe apagar desde el sistema operativo** como si fuera un PC normal. Al apagarse completamente pierde el payload inyectado y vuelve al sistema de Nintendo (HOS).

**Para no perder Linux entre sesiones:**
- Usar **suspender** en lugar de apagar
- Si se apaga, hay que volver a entrar en RCM e inyectar el payload con TegraRcmGUI desde el PC

Esto es el comportamiento normal — el payload no es persistente y debe inyectarse cada vez que la Switch se apague por completo.
