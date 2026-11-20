# Mushi 🐾

Mushi es una mascota que lleva y trae **notas de voz** entre los peques y su familia (abuelos, tíos, padres que están de viaje...), a través de Telegram.
La familia le manda notas desde el móvil; Mushi avisa con los ojos y con su luz, y el peque las escucha con solo pulsar un botón. Para contestar, vuelve a pulsar y habla: la nota llega al grupo de la familia.

### ✨ Cómo lo hemos pensado

- **Sin pantallas que enganchen.** El peque no tiene un móvil ni una tablet: no hay vídeos, juegos, anuncios ni nada que deslizar. La pantalla de Mushi solo muestra sus ojos y lo que siente, y la comunicación es solo con la voz de su familia.
- **Un solo botón.** Todo se hace con un único botón grande: pulsar para escuchar y pulsar para hablar. No hace falta saber leer ni escribir, ni que un adulto le ayude.
- **Solo la familia.** Mushi solo habla con el grupo de Telegram de la familia, y el admin (un adulto de la familia) decide quién está en él. Ningún desconocido puede hablar con el peque.
- **Con sus horarios.** Por la noche duerme: no suena ni molesta, y las notas que llegan esperan a la mañana.
- **Privacidad y seguridad, lo primero.** Es un juguete para niños, y hemos puesto especial atención en protegerlos: conexiones cifradas, actualizaciones firmadas para que nadie pueda modificarlo y control total de la familia. Todos los detalles, en [Privacidad y seguridad](#-privacidad-y-seguridad).

Además, Mushi tiene vida propia: se aburre cuando no hay nadie (y entonces pasan cosas por su pantalla), celebra las fiestas y el cumpleaños, y guarda sorpresas que la familia le deja para una hora concreta.

## 📖 Guía de uso

**[Guía para familias](GUIA.md)**: puesta en marcha en 6 pasos y manual completo (configuración, Telegram, el día a día, sorpresas, comandos y problemas frecuentes).

## ⬇️ Actualizaciones

Mushi se actualiza solo, de madrugada, mientras duerme. Las novedades de cada versión están en **[Releases](../../releases)**.

Cada versión va firmada: Mushi solo instala versiones oficiales de este repositorio.

## 🔒 Privacidad y seguridad

Mushi es para niños, y por eso la privacidad y la seguridad han sido una prioridad desde el primer día. Esto es lo que hace Mushi para proteger a tu familia y lo que conviene que sepas.

### 🎙️ Las notas de voz

- **Mushi solo graba cuando el peque pulsa el botón**, y se ve en la pantalla (punto rojo de grabación). No escucha ni graba nada por su cuenta. No tiene cámara: el radar solo nota si alguien se mueve cerca y el sensor de luz, si hay luz.
- Las notas **solo viajan entre Mushi y el grupo de Telegram de la familia**. Mushi nunca las manda a nadie más ni las guarda en ningún otro sitio.
- Las notas que graba el peque se envían **protegidas**: en Telegram no se pueden reenviar ni guardar.
- Las notas que recibe se guardan en Mushi solo hasta que el peque las escucha, y después se borran.

### 👨‍👩‍👧 Solo la familia

- Mushi **solo atiende a quien está en el grupo**. Si alguien de fuera le escribe por privado, no le contesta a nada (ni a sus mensajes ni a sus notas) y lo bloquea 24 horas.
- **El admin decide quién entra en el grupo.** Si alguien entra sin que el admin lo haya añadido, Mushi le quita los permisos al momento y pregunta al admin si se queda o se va. Con `/grupo enlace`, quien use la invitación no entra ni ve nada hasta que el admin lo permite. Mientras espera, sus notas no le llegan al peque.
- **Los comandos solo los obedece el admin.** Si un comando llega con mucho retraso (por ejemplo, de noche, mientras Mushi duerme), no lo hace por sorpresa: avisa y pregunta.
- `/grupo proteger` deja el grupo para notas de voz y comprueba la privacidad: te dice si falta activar «Restringir guardar contenido».

### 🔐 Conexiones cifradas

- Mushi habla con Telegram siempre por **conexión cifrada (HTTPS)** y comprueba el certificado de Telegram, para estar seguro de que habla con Telegram y no con un impostor.
- Para configurarlo, Mushi crea su propia Wi-Fi, con una contraseña que solo se ve en su pantalla.
- La contraseña de tu Wi-Fi y la clave del bot se quedan en Mushi: no se envían a nadie ni aparecen en su registro.

### ✍️ Actualizaciones firmadas

- Cada versión de Mushi va **firmada digitalmente** (ECDSA P-256), y Mushi la comprueba antes de instalarla. **Un firmware sin la firma correcta no se instala**, venga de donde venga: nadie puede colarle un programa modificado.
- La clave para firmar nunca sale del ordenador de quien publica las versiones: no está en este repositorio ni en ningún otro sitio.
- La firma lleva dentro el número de versión, y Mushi no vuelve a una versión anterior salvo que el admin lo pida a propósito.
- Si una versión nueva no arrancara bien, Mushi **vuelve sola a la anterior**.
- Las actualizaciones automáticas se instalan de madrugada, mientras duerme, y por la mañana avisa al admin.

### 🛟 Soporte

- Para poder ayudar, Mushi apunta en la lista de soporte **su número de serie, el nombre de su bot y su versión. Nada más**: ni nombres, ni mensajes, ni notas. La lista es privada y está protegida: cada Mushi tiene su propia clave y soporte tiene que aprobarlo.
- **Soporte no puede entrar en tu Mushi si tú no le dejas.** Solo con `/remoto on` del admin, durante unas horas (4 de serie), y Mushi avisa al admin cuando se usa.
- En las versiones de pruebas, Mushi manda cada día a soporte su registro técnico: lo que ha hecho, con horas y los nombres de quien manda notas, pero **nunca las notas de voz**. Avisa al admin, se puede parar con `/pruebas off` y se acaba con la versión final.
- Restablecer de fábrica borra todo lo de la familia de Mushi: ajustes, Wi-Fi, bot y notas.

### ℹ️ Conviene saber

- Las notas están en el grupo de Telegram como cualquier mensaje de Telegram, y se guardan en sus servidores según [sus condiciones](https://telegram.org/privacy). Mushi no puede controlar lo que hace Telegram.
- Lo más importante para la seguridad es la **cuenta de Telegram del admin**: activa la verificación en dos pasos (Ajustes → Privacidad y seguridad) y no compartas el código del bot.

## 📦 Contenido del repositorio

- `GUIA.md`: guía de uso para familias.
- **Releases**: el firmware de cada versión (`firmware_firmado.bin`) y sus notas.
