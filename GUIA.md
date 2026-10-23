# Mushi — Guía de uso

Mushi es una mascota que lleva y trae **notas de voz** entre el niño o la niña y su familia, a través de **Telegram**. La familia le manda notas desde el móvil; Mushi avisa con los ojos y con su luz, y el peque las escucha con solo pulsar el botón grande. Para contestar, vuelve a pulsar y habla: la nota llega al grupo de Telegram de la familia.

Además, Mushi tiene vida propia: duerme por la noche, se aburre cuando no hay nadie, celebra las fiestas y el cumpleaños, y de vez en cuando da alguna sorpresa.

> Esta guía corresponde a la versión **v2.6.1**. Las novedades de cada versión están en las [notas de las versiones](../../releases).

---

## Índice

- [Inicio rápido](#inicio-rápido)
- [Manual completo](#manual-completo)
  1. [Lo que necesitas](#1-lo-que-necesitas)
  2. [Configuración: el portal](#2-configuración-el-portal)
  3. [Telegram: el bot y el grupo](#3-telegram-el-bot-y-el-grupo)
  4. [El día a día](#4-el-día-a-día)
  5. [Lo que muestran los ojos](#5-lo-que-muestran-los-ojos)
  6. [Sueño, aburrimiento y sorpresas](#6-sueño-aburrimiento-y-sorpresas)
  7. [Fiestas, cumpleaños y sorpresas](#7-fiestas-cumpleaños-y-sorpresas)
  8. [Comandos de Telegram](#8-comandos-de-telegram)
  9. [Actualizaciones](#9-actualizaciones)
  10. [Problemas frecuentes](#10-problemas-frecuentes)
  11. [Restablecer de fábrica](#11-restablecer-de-fábrica)

---

## Inicio rápido

**1. Enciéndelo.** Conéctalo a un cargador USB. La primera vez, Mushi nace: sale de un huevo y enseguida muestra un código QR.

**2. Conecta el móvil a Mushi.** Escanea el QR con la cámara del móvil, o conéctate a mano a la red Wi-Fi **Mascota-Setup** con la clave que aparece en la pantalla.

**3. Abre el portal.** Normalmente se abre solo. Si no, abre el navegador y entra en **192.168.4.1**.

**4. Rellena lo imprescindible:**
- **Tu Wi-Fi:** toca tu red en la lista y escribe la contraseña. Pulsa **Probar** para comprobarla.
- **El código del bot de Telegram:** el portal te explica cómo crearlo en 2 minutos con @BotFather (ver [apartado 3](#3-telegram-el-bot-y-el-grupo)). Cópialo y pégalo.

**5. Pulsa «Guardar y reiniciar».**

**6. Escanea el QR de la pantalla de Mushi** con el móvil y pulsa **Iniciar** en Telegram. Mushi te contestará con un botón **«Añadirme al grupo de la familia»**: púlsalo, elige el grupo (o crea uno) y acepta. Mushi saluda en el grupo y en su pantalla aparece **«¡Listo!»**.

Todo lo demás viene preparado de serie y se puede cambiar cuando quieras.

---

## Manual completo

### 1. Lo que necesitas

- Mushi y un cargador USB (de móvil vale).
- Una red Wi-Fi de 2,4 GHz (la mayoría de routers la tienen).
- Telegram en el móvil de quien vaya a enviar notas.
- Un **grupo de Telegram** de la familia, donde estará Mushi.

Coloca a Mushi donde el peque pase tiempo y con buena cobertura Wi-Fi. Si la señal es débil, Mushi funciona igual pero puede tardar algo más en recibir y enviar.

### 2. Configuración: el portal

El portal es la página donde se configura todo. Se abre:

- **La primera vez** que se enciende (o tras restablecerlo).
- **Cuando el admin manda `/config`** por Telegram.

En ambos casos, Mushi muestra en la pantalla un QR, el nombre de su red (**Mascota-Setup**) y su clave. Conéctate con el móvil y entra en **192.168.4.1**.

Cada opción tiene un botón **?** que explica qué hace. Las opciones están ordenadas por temas:

| Apartado | Qué se configura |
|---|---|
| **1. Tu Mushi y la Wi-Fi** | Nombre de la mascota y del niño/a, red Wi-Fi principal y una de reserva |
| **2. Telegram** | Código del bot (con el paso a paso para crearlo) |
| **3. Ojos y sonido** | Color de los ojos, volumen, sonido al llegar una nota, aviso cuando la escucha |
| **4. Horario de sueño** | Si duerme por la noche, de qué hora a qué hora, y si saluda al grupo al despertar |
| **5. Presencia y aburrimiento** | Radar, cuándo se aburre, cuándo apaga la pantalla, sorpresas |
| **6. Cumpleaños** | El día del cumple del niño/a |
| **6b. Ranking familiar de la semana** | Si se manda, el día y la hora (por defecto, el domingo 15 minutos antes de dormir) |
| **7. Actualizaciones** | Si se actualiza solo de madrugada |
| **Avanzado** (plegado) | Botón, duración de las notas, esperas, sensibilidad del radar, formato y calidad de las notas, micrófono, borrado de mensajes, batería, soporte remoto, Telegram a mano y «Volver a emparejar» |

**Consejos sobre la Wi-Fi:**
- Pulsa **Buscar** para ver las redes cercanas ordenadas por señal y toca la tuya.
- Pulsa **Probar** antes de guardar: te dirá si la contraseña es correcta.
- Si dejas la contraseña en blanco, se mantiene la que ya estaba guardada.
- La **red de reserva** se usa si la principal falla (por ejemplo, la de un repetidor o la del móvil).

Al pulsar **Guardar y reiniciar**, Mushi aplica los cambios y vuelve a arrancar.

### 3. Telegram: el bot y el grupo

Mushi usa un **bot de Telegram** propio. Solo hay que crearlo una vez; del resto se encarga Mushi.

**Crear el bot** (el portal lo explica paso a paso):
1. En Telegram, abre **@BotFather** y pulsa **Iniciar**.
2. Escríbele `/newbot`.
3. Elige un nombre, por ejemplo *Mushi de Mateo*.
4. Elige un usuario que acabe en **bot**, por ejemplo *mushi_de_mateo_bot* (si ya existe, prueba otro).
5. BotFather te da un código largo, como `123456789:ABCdef...`. Cópialo y pégalo en el portal.

**Emparejar** (sin copiar ningún número):
1. Al guardar, Mushi enseña en su pantalla un **QR** y un código de 4 cifras.
2. Escanéalo con el móvil y pulsa **Iniciar** en Telegram: quedas como **admin** (la persona que puede cambiar los ajustes por Telegram).
3. Mushi te contesta con el botón **«Añadirme al grupo de la familia»**. Púlsalo, elige el grupo de la familia (o crea uno nuevo) y acepta hacerlo **administrador**: lo necesita para oír las notas de voz del grupo.
4. Mushi saluda en el grupo y en su pantalla aparece **«¡Listo!»**.

Si no puedes escanear el QR, busca tu bot en Telegram y escríbele `/start` seguido del código de 4 cifras de la pantalla.

**Volver a emparejar** (para cambiar de grupo o de admin): en el portal, apartado **Avanzado**, marca **«Volver a emparejar con Telegram»** y guarda. Al reiniciar, Mushi enseñará otra vez el QR.

### 4. El día a día

**Cuando llega una nota:**
- Mushi suena (un ding-dong), sus ojos cambian y **la luz del botón grande se queda encendida**.
- Si hay varias, las va guardando en orden.

**Para escucharla:** el peque pulsa el botón grande. Se reproduce la nota más antigua; si hay más, vuelve a pulsar.
Si está activado, quien mandó la nota recibe en Telegram un aviso de que ya la ha escuchado.

**Para grabar una nota:** con todas las notas escuchadas, el peque pulsa el botón grande, habla y vuelve a pulsar para terminar.
- Mientras graba, en la pantalla se ven los segundos: verdes, luego amarillos y rojos al final.
- Al llegar al tiempo máximo (60 s de serie), la nota se envía sola.
- Las grabaciones demasiado cortas (un toque sin querer) se descartan.
- Si en ese momento no hay Internet, la nota se guarda y se envía en cuanto vuelva la conexión.

**Los dos botones pequeños** son para los mayores (para despertarlo de noche y para restablecerlo); el peque solo necesita el grande.

### 5. Lo que muestran los ojos

| Lo que ves | Qué significa |
|---|---|
| Ojos abiertos que miran y parpadean | Despierto, esperando |
| Ojos con sobres y la luz del botón encendida | Hay notas por escuchar (el número de abajo a la derecha dice cuántas) |
| Ojos con una caja de regalo | Hay una sorpresa: pulsa para abrirla (abajo a la izquierda, un regalito con cuántas hay) |
| Contador de segundos de colores | Está grabando |
| Ojos entornados | Aburrido: hace un rato que no ve a nadie |
| Ojos curvados que respiran, con Zzz | Durmiendo |
| Adornos de fiesta | Hoy es un día especial |
| «Actualizando… ¡No lo apagues!» | Instalando una versión nueva: no lo desenchufes |

### 6. Sueño, aburrimiento y sorpresas

**Horario de sueño.** De serie, Mushi duerme de **21:00 a 8:00**: ojos cerrados, sin sonidos ni avisos. Las notas que lleguen de noche se guardan y las verá por la mañana. Al despertar hace una pequeña animación (sin melodía, para no molestar).

**Buenos días y buenas noches en el grupo.** Al dormirse, Mushi avisa en el grupo ("🌙 Mateo se va a dormir hasta las 8:00…"). Y al despertar saluda: "☀️ ¡Buenos días! Mateo ya está despierto. Tiene 3 notas esperando para escuchar 📬" (si no tiene ninguna, os anima a mandarle una). Espera un minuto y medio tras despertar, para recoger antes las notas de la noche y que el número sea el real. El saludo se quita con `/sueno saludo off` (y vuelve con `/sueno saludo on`), con su botón en la sección Sueño del panel (`/menu`) o con su casilla en el portal (apartado 4).

- **Despertarlo una noche especial:** mantén pulsados **a la vez los dos botones pequeños durante 3 segundos**. Se despierta y sigue despierto el resto de la noche; el admin recibe un aviso. Para volver a dormirlo, el admin manda `/dormir`.
- **Encender la pantalla si alguien se mueve de noche:** opción del apartado 4 del portal (necesita el radar).

**Aburrimiento.** Mushi tiene un radar que nota si hay alguien cerca.
- Si pasa un rato sin nadie (**5 minutos** de serie), se aburre. Mientras se va aburriendo, la pantalla baja de brillo poco a poco.
- Aburrido, de vez en cuando aparece una **sorpresa** por la pantalla y Mushi la sigue con la mirada: burbujas, un pajarito, una mariposa, hojas que caen, nieve, lluvia con arcoíris, un globo… (¡y muy de vez en cuando, algo más raro!). Las sorpresas cambian según la estación del año.
- Tras un rato aburrido (**5 minutos** de serie), apaga la pantalla para ahorrar.
- En cuanto ve a alguien, se pulsa un botón o llega una nota, se despierta.

Todos estos tiempos se cambian en el apartado 5 del portal o con `/aburrido`.

### 7. Fiestas, cumpleaños y sorpresas

Mushi celebra solo las fiestas del año (Navidad, Reyes, Halloween…): esos días se adorna y, de vez en cuando, tiene un momento especial.

Si pones el **cumpleaños** del niño/a en el portal (apartado 6) o con `/cumple`, ese día lo celebra todo el día.

**Notas solo de tu parte y sorpresas** 🎁: cualquier familiar del grupo puede mandarle al peque una nota que el resto del grupo no vea, ya o a una hora concreta (un "buenas noches", una felicitación…).

1. Abre el **chat privado con el bot de Mushi** (no el grupo) y manda la nota de voz, como siempre.
2. Mushi te pregunta cuándo dársela, con botones:
   - **▶️ Ahora:** le llega ya, como una nota normal, pero el grupo no la ve.
   - **A una hora** (⏰ En 1 hora, 🌙 Esta noche, ☀️ Mañana, o escribe tú la hora, como `19:30`): le llega como **sorpresa**. A esa hora aparece una **caja de regalo** en los ojos de Mushi; cuando el peque pulsa el botón, se abre con confeti y suena la nota.
3. Te llegan avisos por privado: con una sorpresa, **cuando le llega a Mushi** (aparece la caja de regalo) y **cuando la abre**; con una nota "Ahora", cuando la escucha.

Ten en cuenta que **si el peque contesta, su respuesta va al grupo** de la familia y la escuchan todos.

Las sorpresas pasan delante de las notas que estuvieran esperando y tienen sus propios huecos en el buzón, así que llegan a su hora aunque haya muchas notas sin escuchar (si aun así no cabe, Mushi te avisa y la entrega en cuanto haya sitio). Mientras hay sorpresas esperando, abajo a la izquierda de la pantalla brilla un regalito con su número. Si a esa hora Mushi duerme, la sorpresa espera a que se despierte. Para ver o cancelar las que has programado, escribe `/sorpresas` en el chat privado con el bot.

**Menú de comandos:** en Telegram, el botón **/** junto al cuadro de texto muestra los comandos que puedes usar, con su explicación. Tócalos en lugar de escribirlos.

**Ranking familiar de la semana 🏆:** por defecto, cada domingo, 15 minutos antes de la hora de dormir, Mushi manda al grupo quién mandó más notas (con medallas), quién habló más, quién preparó más sorpresas, quién fue el madrugador y lo que escuchó y contestó el peque. Con `/ranking` lo ves cuando quieras.

### 8. Comandos de Telegram

Los comandos los puede usar **el admin**, en el grupo o en privado con el bot. Las respuestas a comandos en el grupo se borran solas al cabo de unos minutos para no llenarlo.

Si escribes mal un comando, Mushi te avisa y te sugiere el correcto. `/ajustes` muestra todos los ajustes y cómo cambiarlos.

**Estilos de ojos.** Además del color, Mushi puede tener estilo, y se combinan entre sí (180 combinaciones):

- **Clásico:** los ojos de siempre.
- **Pestañas:** tres por ojo, que siguen al párpado al parpadear.
- **Cejas:** cambian con su ánimo: levantadas cuando tiene notas esperando y caídas cuando se aburre.
- **Lazo:** un lazo rosa arriba a la izquierda (violeta si los ojos son rosas o fucsia).
- **Gafitas:** gafas redondas.
- **Estrellas** y **Corazones:** los brillos de los ojos con esa forma (con Corazones, también el destello del sobre de la nota nueva).
- **Dibujos animados:** ojos tiernos, con un iris grande y brillante del color elegido. Cambian con su ánimo: sonrientes cuando tiene notas o una sorpresa, con el párpado medio caído cuando se aburre, de cachorrito cuando está triste y bien abiertos cuando te escucha.
- **Uno cada día:** cambia de estilo cada día (y con el color en "uno cada día", cada día sale una combinación distinta).

Se ven en todas las pantallas con ojos (también con los sobres, el regalo, al grabar, al cargar, en los ajustes, durmiendo, triste o aburrido), y las cejas ponen la cara de cada momento. Se elige con `/estilo`, en la sección ✨ Estilo del panel o en el portal (apartado 3), donde una **vista previa** enseña cómo quedan los ojos al elegir el color y el estilo. Los días de fiesta (cumple, Navidad, Halloween...) el estilo se combina con la decoración; cuando la fiesta pone un gorro, una corona o un antifaz sobre los ojos, todo se queda (los gorros y la corona van en el ojo derecho, encima de las gafitas si las lleva), salvo la ceja de ese ojo, que sale solo en el otro (y con el antifaz de Carnaval o los huevos de Pascua, todo eso se aparta mientras duran).

**El panel con botones (`/menu`).** Si prefieres tocar en vez de escribir, envía `/menu` y Mushi te manda por privado un panel: un solo mensaje con botones que se actualiza al pulsar. Secciones:

- **📊 Estado:** lo que está haciendo, notas sin escuchar, Wi-Fi, batería, versión.
- **✨ Estilo:** el estilo de los ojos.
- **🎨 Ojos y sonido:** color (19 colores, arcoíris o uno cada día), volumen, sonido al llegar una nota, aviso de "ha escuchado", y la melodía del despertar (volumen, timbre y un botón para escucharla).
- **🌙 Sueño:** activarlo y las horas, con ◀️ ▶️.
- **📡 Radar:** activo, sensibilidad, de noche, cuándo se aburre, cuánto tarda aburrido en apagar la pantalla, y si salen sorpresas al aburrirse y cada cuánto.
- **🎁 Sorpresas:** las que hay programadas, con un botón para cancelar cada una.
- **🏆 Ranking:** si se manda, el día y la hora (automática o fija, de 30 en 30 min).
- **🎂 Cumple:** el cumple y la fiesta de hoy, borrar el cumple, y silenciar 1, 2 u 8 horas.
- **🎙️ Micro:** la ganancia (bájala si las grabaciones saturan), la duración máxima y mínima de una grabación, el modo de grabar, la calidad y las esperas tras escuchar y tras enviar.
- **🔋 Batería:** activarla, el ahorro de noche y el detector de cargador.
- **🛠️ Mantenimiento:** buscar o instalar actualizaciones, las actualizaciones automáticas, el estado completo, el log, volver a dormirlo, apagarlo, abrir el portal y reiniciar. Instalar, apagar, abrir el portal y reiniciar piden confirmación; lo que contestan llega como mensaje aparte.

Al tocar un botón, Mushi hace lo mismo que con el comando escrito, te lo confirma con un aviso en la pantalla del móvil y el panel muestra los valores nuevos. Solo lo puede usar el admin. Algunas cosas se siguen escribiendo, como el día del cumple (`/cumple 14/05`) o calibrar la batería; borrar todo (`/resetall`) no está en el panel, a propósito.

**Ajustes básicos**

| Comando | Qué hace |
|---|---|
| `/menu` | Panel con botones para cambiar los ajustes |
| `/ajustes` | Ver todos los ajustes |
| `/volumen 70` | Volumen (0-100) |
| `/color rosa` | Color de los ojos: turquesa, verde, amarillo, morado, rosa, naranja, rojo, azul, lila, lima, blanco, menta, celeste, coral, dorado, fucsia, violeta, aguamarina, melocotón, arcoíris (va cambiando de color), o `/color cada día` (uno distinto cada día) |
| `/estilo cejas` | Estilo de los ojos: clásico, pestañas, cejas, lazo, gafitas, estrellas, corazones, animado (dibujos animados), o `/estilo cada día`. Se combina con cualquier color |
| `/nombre Mushi` | Nombre de la mascota |
| `/nino Mateo` | Nombre del niño/a (`/nino borrar` para quitarlo) |
| `/aviso on` / `off` | Sonido al llegar una nota |
| `/confirmacion on` / `off` | Avisar a quien mandó la nota cuando se escucha |

**Sueño y aburrimiento**

| Comando | Qué hace |
|---|---|
| `/sueno 21-8` | Horario de sueño (`/sueno on` / `off` para activarlo o quitarlo) |
| `/sueno saludo off` | Quitar el saludo de buenos días al grupo (`on` para volver a ponerlo) |
| `/dormir` | Volver a dormirlo si se le ha despertado de noche |
| `/silencio 2` | Silencio durante 2 horas (sin sonidos; los ojos avisan igual). `/silencio off` para acabar |
| `/aburrido` | Ver la configuración del aburrimiento |
| `/aburrido 5` | Minutos sin nadie hasta aburrirse |
| `/aburrido pantalla 5` | Minutos aburrido hasta apagar la pantalla |
| `/aburrido sorpresas on` / `off` | Poner o quitar las sorpresas |
| `/aburrido sorpresas 2 5` | Una sorpresa cada 2 a 5 minutos, al azar |
| `/radar on` / `off` | Detectar si hay alguien |

**Fiestas**

| Comando | Qué hace |
|---|---|
| `/cumple 5/3` | Cumpleaños (día/mes). `/cumple borrar` para quitarlo |
| `/fiesta` | Ver qué fiesta es hoy |
| `/despertar` | Hacer la animación de despertar ahora |
| `/sorpresas` | Ver o cancelar las sorpresas programadas (en el chat privado con el bot) |
| `/ranking` | Ver el ranking de la semana |
| `/ranking dia lunes` | Cambiar el día en que se envía al grupo |
| `/ranking hora 20:30` | Cambiar la hora de envío (`/ranking auto` para volver a la automática) |

**Sistema**

| Comando | Qué hace |
|---|---|
| `/status` | Estado y diagnóstico |
| `/test` | Autotest: revisa todo el hardware, la red y el sistema (unos 2 minutos) y te manda el informe por privado |
| `/config` | Abrir el portal de configuración |
| `/actualizar comprobar` | Ver si hay una versión nueva |
| `/reiniciar` | Reiniciarlo |
| `/apagar` | Apagar la pantalla hasta tocar el botón (`/apagar 3h` durante 3 horas) |
| `/salida` | Ver las notas grabadas que esperan a enviarse |
| `/remoto on` | Abrir el soporte remoto unas horas, para que te puedan ayudar |
| `/resetall` | Restablecer de fábrica (pide confirmación) |

### 9. Actualizaciones

Mushi se mantiene al día solo:

- **De madrugada** (entre las 3:00 y las 4:30), mientras duerme, comprueba si hay una versión nueva. Si la hay, la instala con la pantalla apagada y por la mañana avisa al admin.
- Solo instala versiones oficiales: cada versión va **firmada** y Mushi comprueba la firma antes de instalarla.
- Si algo fallara, vuelve solo a la versión anterior.

Mientras se instala por otro medio, la pantalla muestra **«¡No lo apagues!»** y una barra de progreso: **no lo desenchufes** hasta que termine (tarda alrededor de un minuto).

Para ver si hay novedades en cualquier momento: `/actualizar comprobar`. Para desactivar las actualizaciones automáticas, quita la casilla del apartado 7 del portal.

### 10. Problemas frecuentes

**Antes de nada, el autotest.** Envía `/test` por privado al bot (o mantén pulsado el botón lateral pequeño 5 segundos). Mushi revisa en unos 2 minutos todo lo que puede fallar, con una pantalla por paso que se va rellenando: la pantalla y el LED, el altavoz y el micrófono (pita y se escucha a sí mismo), el botón grande (te pide pulsarlo), que los botones pequeños no estén atascados, el radar (te pide moverte delante), el sensor de luz (te pide taparlo), la batería, el Wi-Fi, la red (router, DNS e Internet), Telegram, la hora, las actualizaciones, la temperatura, la memoria y los ajustes que conviene revisar. Al final enseña el resultado y te manda un informe con todo lo medido: ✅ bien, ⚠️ aviso, ❌ fallo. Con ese informe se ve enseguida dónde está el problema.

**No se conecta a la Wi-Fi.**
Comprueba que la red es de 2,4 GHz y la contraseña es correcta (usa **Probar** en el portal). Si Mushi no consigue conectarse, sigue intentándolo solo; si cambiaste de router, abre el portal y elige la red nueva.

**No le llegan las notas.**
Comprueba que el bot está en el grupo y que la nota se manda a ese grupo. Si Mushi está durmiendo, las notas esperan a la mañana.

**No suena.**
Mira el volumen (`/volumen`), que no esté en silencio (`/silencio off`) y que no sea su hora de dormir.

**La pantalla está apagada.**
Puede estar aburrido (no hay nadie) o durmiendo. Pulsa el botón grande o acércate: se despierta.

**Las notas que graba se oyen muy bajas o saturadas.**
Ajusta el *Volumen del micrófono* en el apartado Avanzado del portal.

**Se ha quedado bloqueado.**
Desenchúfalo unos segundos y vuelve a enchufarlo. No pierde las notas ni los ajustes.

**El código del bot no es correcto.**
Si al reiniciar Mushi dice que el código del bot no es correcto, vuelve a abrir el portal y pégalo otra vez, entero (con los dos puntos). Si lo has perdido, en @BotFather escribe `/mybots`, elige tu bot y pulsa *API Token*.

**Necesito ayuda.**
Activa el soporte remoto (`/remoto on`, o la casilla del apartado Avanzado del portal): permite revisar tu Mushi a distancia durante unas horas y se cierra solo.

### 11. Restablecer de fábrica

Borra todos los ajustes (Wi-Fi, Telegram, nombres…) y Mushi vuelve a nacer como el primer día.

- **Por Telegram:** el admin manda `/resetall` y confirma.
- **Con los botones:** mantén pulsado el **botón lateral pequeño** mientras lo enchufas. En la pantalla aparece la pregunta: el **botón BOOT acepta** y el lateral cancela (si no se pulsa nada en 30 segundos, se cancela solo).

Después, configúralo de nuevo como en el [Inicio rápido](#inicio-rápido).
