<div align="center">

# LucsysOS

**Una edición de Windows 11 Pro preparada para trabajar desde el primer arranque.**

[Últimas versiones](../../releases) · [Actualizaciones](#actualizaciones) · [Seguridad](#seguridad)

</div>

---

## Descripción

LucsysOS es una imagen de instalación de Windows 11 Pro con configuración propia y **LucsysOS Panel**, una aplicación de gestión del sistema que reúne en un solo lugar lo que normalmente está repartido entre Configuración, el Panel de control y herramientas de terceros.

Durante la instalación, un asistente permite elegir la **versión** de LucsysOS que mejor se adapta al uso del equipo:

| Versión | Orientada a |
|---|---|
| **LucsysOS** | Uso general, con la configuración estándar |
| **ZEN** | Portátiles: autonomía, silencio y cuidado de la batería |
| **PRO** | Rendimiento sostenido y monitorización en tiempo real |
| **DEV** | Desarrollo: gestión de entornos (Java, Node.js, Python, Go, .NET, Git) |
| **ADM** | Administración de cuentas locales, funciones y directivas |
| **VM** | Ejecución dentro de máquinas virtuales |

Cada versión es reversible y se puede cambiar más adelante desde el panel.

## LucsysOS Panel

- **Energía y rendimiento:** modos de energía, gráfica dedicada, reglas por proceso y asignación de GPU por aplicación.
- **Virtualización:** cambio entre Hyper-V y rendimiento nativo para VirtualBox y VMware.
- **Mantenimiento:** controladores, puntos de restauración, diagnóstico de salud con informe y utilidades verificadas.
- **Dispositivos y datos:** gestión de memorias USB, pruebas de capacidad real y sincronización de carpetas.
- **Personalización:** temas, fondos de escritorio y de pantalla de bloqueo generados para cada tema, e imágenes propias.
- **Configuraciones portables:** exportación de la configuración para aplicarla en otro equipo o durante la instalación.

## Actualizaciones

Las actualizaciones de LucsysOS Panel y de sus componentes se distribuyen como paquetes `.lucsysupd` en la sección [Releases](../../releases).

- **Automáticas:** el panel comprueba si hay una versión nueva desde *Configuración › Acerca de › Actualizaciones de LucsysOS*, y el agente del sistema avisa una vez al día cuando hay una disponible.
- **Manuales:** también se puede descargar el paquete de la release e instalarlo con *Instalar desde archivo…*.
- **Sin interrupciones:** la instalación cierra y vuelve a abrir el panel automáticamente; si algo falla, se restaura la versión anterior.

Las imágenes de instalación (ISO) se publican por separado cuando hay cambios de mayor alcance.

## Seguridad

- **Paquetes firmados.** Cada actualización incluye un manifiesto firmado digitalmente (ECDSA P-256) con el hash SHA-256 de cada archivo. LucsysOS Panel lleva incorporada la clave pública y verifica la firma y el contenido completo antes de instalar.
- **Sin modificaciones ni archivos añadidos.** Un paquete alterado, incompleto o con archivos que no estén en el manifiesto se rechaza.
- **Sin versiones anteriores.** No se puede instalar una versión más antigua que la instalada, lo que impide reintroducir fallos ya corregidos.
- **Actualizaciones de seguridad.** Las releases marcadas como **[seguridad]** corrigen vulnerabilidades del panel o de sus scripts; el sistema las destaca y se recomienda instalarlas cuanto antes.
- **Instalación protegida.** El paquete se copia y se vuelve a verificar en una carpeta a la que solo tienen acceso los administradores antes de aplicarse.

---

<sub>LucsysOS es un proyecto independiente y no está afiliado a Microsoft. Windows es una marca registrada de Microsoft Corporation.</sub>