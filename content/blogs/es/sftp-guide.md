---
title: Guía de Conexión a SFTP [2025]
date: "2025-08-21"
authorId: "teoremal-dev"
excerpt: "Aprende a conectar tus archivos a Teramont.net mediante SFTP con WinSCP, FileZilla y CyberDuck de forma rápida y segura."
category: "Tutoriales"
tags: [SFTP, WinSCP, FileZilla, CyberDuck, Seguridad, Servidores, Tutorial]
---

# Cómo Usar Clientes SFTP en Teramont.net: WinSCP, FileZilla y CyberDuck

:::info
Este tutorial está diseñado para usuarios de Teramont.net que deseen conectar sus archivos mediante SFTP utilizando el Teramont Control Panel (TCP). Nos enfocaremos exclusivamente en SFTP, ya que el panel maneja automáticamente la configuración necesaria. Asegúrate de tener tus credenciales listas antes de comenzar.
:::

## Introducción a SFTP en Teramont.net

SFTP (SSH File Transfer Protocol) es un protocolo seguro para transferir archivos entre tu computadora y el servidor de Teramont.net. A diferencia de FTP, SFTP cifra la conexión, protegiendo tus datos. En Teramont.net, el acceso SFTP se configura fácilmente a través del Teramont Control Panel (TCP).

Para obtener tus credenciales SFTP:
1. Inicia sesión en tu panel TCP en [https://panel.teramont.net](https://panel.teramont.net).
2. Ve a la sección **Settings** en el servidor del cual deseas conectarte.
3. En el apartado **SFTP Details**, encontrarás:
    - **Server Address**: Por ejemplo, `sftp://mia05.teramont.net:2022` (el subdominio puede variar según tu servidor).
    - **Username**: Un identificador único, como `ujmtg9pne3715212`.
    - **Password**: Usa la misma contraseña que utilizas para acceder al panel TCP.

¡Toma nota! El botón "Launch SFTP" en el panel TCP te llevará directamente a la configuración de SFTP, desplegará rápidamente WinSCP.

![Captura de pantalla del panel TCP mostrando detalles SFTP](https://imgur.com/oRWlSvL.png)

:::warning
No compartas tus credenciales SFTP con nadie, ya que permiten acceso completo a tus archivos. En su lugar, puedes crear Sub-Usuarios.
:::

> [!TIP]  
> Siempre actualiza tus clientes SFTP a la versión más reciente para mayor seguridad.

A continuación, te guiaremos paso a paso para conectar usando tres clientes populares: WinSCP (para Windows), FileZilla (multiplataforma) y CyberDuck (para macOS y Windows).

## Conectando con WinSCP

WinSCP es un cliente SFTP gratuito y de código abierto, ideal para usuarios de Windows. Descárgalo desde [https://winscp.net](https://winscp.net).

### Pasos para conectar:
1. Instala y abre WinSCP. Se abrirá el diálogo de "Login".
2. En "Protocolo", selecciona **SFTP**.
3. En "Nombre o IP del servidor", ingresa el nombre del host sin el prefijo (por ejemplo, `mia05.teramont.net`).
4. En "Puerto", ingresa **2022** (o el puerto indicado en tu panel).
5. En "Usuario", ingresa tu username (por ejemplo, `ujmtg9pne3715212`).
6. En "Contraseña", ingresa la contraseña de tu panel TCP.
7. Opcional: Presiona "Guardar" para guardar la sesión con un nombre como "Mi servidor Extreme 6GB".
8. Haz clic en "Conectar" para conectar.

![Captura de pantalla del diálogo de Login en WinSCP](https://imgur.com/IxFsefF.png)

:::danger
Si recibes un error de conexión, verifica que el puerto sea correcto (2022 en lugar del predeterminado 22) y que no haya firewalls locales bloqueando la salida.
:::

Una vez conectado, verás los archivos remotos en el panel derecho y locales en el izquierdo. Arrastra y suelta para transferir.

> [!WARNING]  
> Evita transferir archivos sensibles sin cifrado adicional si es necesario.

## Conectando con FileZilla

FileZilla es un cliente SFTP gratuito y multiplataforma. Descárgalo desde [https://filezilla-project.org](https://filezilla-project.org).

### Pasos para conectar (usando Quick Connect):
1. Abre FileZilla.
2. En la barra superior "Quick Connect":
    - **Servidor**: Ingresa `sftp://mia05.teramont.net` (incluye el prefijo `sftp://`).
    - **Nombre de usuario**: Ingresa tu username (por ejemplo, `ujmtg9pne3715212`).
    - **Contraseña**: Ingresa la contraseña de tu panel TCP.
    - **Puerto**: Ingresa **2022**.
3. Haz clic en "Conexión rápida".

### Alternativa: Usando Site Manager para conexiones guardadas:
1. Ve a "File" > "Site Manager".
2. Crea una nueva entrada:
    - **Protocolo**: Selecciona SFTP.
    - **Servidor**: `mia05.teramont.net`.
    - **Puerto**: **2022**.
    - **Tipo de inicio**: Normal.
    - **Usuario**: Tu username.
    - **Contraseña**: Tu contraseña.
3. Haz clic en "Conexión rápida".

![Captura de pantalla de Quick Connect en FileZilla](https://imgur.com/AEj3jB3.png)

:::tip
FileZilla guarda las últimas 10 conexiones Quick Connect para reutilizarlas fácilmente.
:::

> [!CAUTION]  
> No uses SFTP en redes públicas sin VPN para evitar riesgos.

## Conectando con CyberDuck

CyberDuck es un cliente SFTP gratuito, popular en macOS pero disponible también para Windows. Descárgalo desde [https://cyberduck.io](https://cyberduck.io).

### Pasos para conectar:
1. Abre CyberDuck y selecciona "Archivo" > "Conectar" o haz clic en el botón de nueva conexión.
2. En el dropdown de protocolo, selecciona **SFTP (SSH Transferencia de archivos segura)**.
3. En "Servidor", ingresa el host (por ejemplo, `mia05.teramont.net`).
4. En "Puerto", ingresa **2022** (el default es 22, así que cámbialo si es necesario).
5. En "Nombre de usuario", ingresa tu username (por ejemplo, `ujmtg9pne3715212`).
6. En "Contraseña", ingresa la contraseña de tu panel TCP.
7. Haz clic en "Conectar". Si es la primera vez, acepta la clave del host.

![Captura de pantalla del diálogo de conexión en CyberDuck](https://imgur.com/mqlaXbm.png)

:::info
CyberDuck soporta bookmarks para guardar conexiones frecuentes. Agrega uno después de conectar exitosamente.
:::

## ¡Ya me he conectado! ¿Qué sigue?
Simplemente realiza arrastrados y soltados para transferir archivos entre tu computadora y el servidor. Puedes editar archivos directamente si tu cliente lo permite. Afortunadamente todos estos permiten editar archivos directamente.

## Notas finales

Con estos pasos, podrás acceder y gestionar tus archivos en Teramont.net de manera segura usando SFTP. Si encuentras problemas, verifica tus credenciales en el panel TCP o contacta al soporte de Teramont. Recuerda que SFTP es ideal para editar y cargar archivos, sobre todo aquellos que son pesados (100MB+), permitiendo ediciones rápidas y seguras.

:::danger
Si olvidas tu contraseña, resétala en el panel TCP, ya que es la misma para SFTP.
:::