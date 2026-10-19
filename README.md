<div align="center">

# 👻 Caspr

Panel en el notch de macOS para ver y controlar tus sesiones de Claude Code, Codex y Cursor, con música, bandeja de archivos y más.

<br />

![macOS](https://img.shields.io/badge/macOS-14%2B-007AFF?style=flat-square&logo=apple&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude%20Code-integrado-D97757?style=flat-square)

</div>

---

## 📑 Índice

- [Instalar y empezar (testers)](#-instalar-y-empezar-testers)
- [Qué muestra](#-qué-muestra)
- [Conectar con Claude Code](#-conectar-con-claude-code)
- [Privacidad](#-privacidad)
- [Licencia](#-licencia)

---

## 📥 Instalar y empezar (testers)

> **Necesitas:** un Mac con macOS 14 (Sonoma) o superior y, para la parte de Claude, [Claude Code](https://docs.claude.com/en/docs/claude-code) instalado. Está pensado para Macs con notch; en uno sin notch dibuja una zona simulada arriba (no probado).

1. **Descarga el DMG** de la [última versión](https://github.com/0x-Crisbanks/Caspr/releases/latest) (`Caspr-<versión>.dmg`). No hace falta cuenta de GitHub.
2. **Ábrelo** con doble clic y **arrastra Caspr a Aplicaciones**.
3. **Abre Caspr** desde Aplicaciones. Está firmada y notarizada por Apple, así que no debería mostrar avisos de seguridad. No tiene icono en el Dock: vive en el notch y en un icono de la barra de menús.
4. **Sigue la ventana de bienvenida** (tres pasos). Se puede reabrir desde el icono de la barra de menús → *Bienvenida…*.
5. **Pasa el cursor por el notch** para abrir el panel. También puedes abrirlo o fijarlo con **⌥⌘O**.

### 🔄 Actualizaciones

Caspr busca versiones nuevas por sí solo, al arrancar y cada pocas horas mientras sigue abierto (se puede desactivar en Ajustes → Acerca de, donde también hay *Buscar actualizaciones*). Cuando hay una:

1. Llega **una notificación** («Caspr 0.4.0 disponible») y aparece **un botón con el número de versión** en la cabecera del notch, junto al fantasma.
2. Pulsas el botón: descarga la versión y la comprueba (firma válida, mismo desarrollador y notarizada por Apple; si algo no cuadra, no se instala).
3. El botón pasa a **Reiniciar app**: al pulsarlo, Caspr se sustituye por la versión nueva y se abre. No hay que descargar el DMG ni arrastrar nada.

Las versiones anteriores a la 0.3 no tienen actualizador: se instala la 0.3 o posterior a mano una vez.

### 🌐 Idioma

Español por defecto, con inglés incluido. Se cambia en Ajustes → General → Idioma (también puede seguir el idioma de macOS) y se aplica al reiniciar Caspr.

### 💬 Responder a Claude desde el panel

Pulsa una sesión de Claude y escribe en el campo *Responder a Claude…*: el mensaje se teclea en la terminal de esa sesión, como si lo escribieras ahí.

- **Terminal e iTerm:** se escribe en la pestaña exacta de la sesión (se localiza por su tty). Pide el permiso de Automatización.
- **Warp y otras terminales con una ventana por sesión** (Ghostty, Alacritty…): Claude Code titula la ventana `✳ <nombre de la sesión>`; Caspr la encuentra por ese título en el menú *Ventana* de la app, la trae al frente, comprueba que la ventana enfocada es la de la sesión y solo entonces escribe. Si hay dos ventanas con el mismo título, o no la encuentra, **no escribe nada**. Pide el permiso de **Accesibilidad**. Probado con Warp.
- **VS Code, Cursor y otros editores:** no. Todas sus terminales comparten el título de la ventana, así que no se puede saber cuál es la sesión; Caspr lo dice en vez de arriesgarse.
- Requisito: la sesión debe tener nombre (por ejemplo con `/rename`) para que el título la identifique.
- No se ofrece mientras haya un permiso o una pregunta esperando: esos se contestan en su tarjeta.

### 🔗 Conectar con Claude Code (opcional, recomendado)

Sin conectar ya ves tus sesiones, el cupo de la cuenta y el contexto. Conectar añade aprobar permisos y responder preguntas desde el notch.

1. Icono de la barra de menús → **Ajustes → Claude Code → Conectar…**
2. Revisa la vista previa: muestra exactamente qué se añade a `~/.claude/settings.json`. Antes de escribir se guarda una copia de seguridad.
3. **Abre sesiones nuevas de Claude Code.** Las que ya estaban abiertas no cargan los cambios.

Para deshacerlo: **Desconectar** (solo quita las entradas de Caspr).

### 🔒 Permisos de macOS

Caspr no pide nada al arrancar: macOS los solicita la primera vez que usas cada función, y puedes decir que no sin que el resto deje de funcionar.

| Función | Permiso | Cuándo aparece |
| :-- | :-- | :-- |
| Música y portada | Automatización (Música, Spotify) | Al reproducir música |
| Calendario | Calendarios | Al abrir la pestaña Calendario |
| Espejo | Cámara | Al abrir la pestaña Espejo |
| Saltar a la terminal de una sesión o responderle (Terminal, iTerm) | Automatización | Al pulsar ↗ o enviar una respuesta |
| Sustituir el HUD de volumen y brillo, o responder a una sesión en Warp y similares | Accesibilidad | Al activar el HUD, o al enviar la primera respuesta |

Si negaste uno por error: Ajustes del Sistema → Privacidad y seguridad

### ❓ Problemas frecuentes

- **No veo el panel:** pasa el cursor por el notch o pulsa ⌥⌘O. Si el tamaño no coincide con tu pantalla, ajústalo en Ajustes → Notch.
- **Claude no aparece o el estado va con retraso:** conecta desde Ajustes y abre una sesión nueva de Claude Code.
- **No hay cupo de la cuenta ("Capacity unavailable"):** Caspr lo lee de Claude Code, nunca lo inventa. Si ya tenías otra status line configurada, no la toca y el cupo exacto no estará disponible.
- **Quiero que arranque con el Mac:** Ajustes → Sistema → *Abrir al iniciar sesión*.
- **Desinstalar:** Desconectar en Ajustes, salir desde la barra de menús y borrar Caspr de Aplicaciones. Lo que guarda vive en `~/Library/Application Support/NotchGhost`.

### 🧪 Qué ayudaría que probaras

Es una versión de prueba y no se ha probado todavía en un Mac distinto al de desarrollo. Cuéntanos sobre todo: si la instalación y la bienvenida se entienden, si Conectar funciona en tu Claude Code, y qué permiso o pestaña falla.

---

## ✨ Qué muestra

- **Notch cerrado**: se adapta a lo que pasa. Con sesiones de Claude vivas muestra el fantasma (con el contador de activas cuando las hay); con música, la portada y las barras; si ambas están en marcha, una píldora combinada; un cambio de volumen lo muestra un instante; y si Claude necesita una decisión (permiso o pregunta), **el panel se abre solo**. Sin nada que mostrar, es solo el notch físico. El fantasma en reposo se puede desactivar en `showIdleGhost`.
- **Claude** (pestaña): cada sesión con Caspr (el fantasma: reposo, trabajando, esperando, completada, error), proyecto, chips de modelo/modo de permisos (Manual, Plan, Automático, Aceptar ediciones…), `Goal` si hay un `/goal` activo, anillo de contexto y antigüedad, y su estado. Al pulsar una tarjeta se ve **En vivo** lo mismo que la terminal de Claude Code, leído del transcript: `● Update(archivo)` con `⎿ Added 1 line, removed 1 line`, `● Ran 2 shell commands` (verde al terminar, gris en curso, rojo si falla), el texto de Claude y la línea `✱ Trabajando… (2m 0s · ↓ ~8.1k tokens)` (los tokens son una estimación). Solo se lee el transcript de la tarjeta abierta. La flecha ↗ lleva a su terminal (Terminal e iTerm eligen la pestaña exacta por tty; Warp, VS Code y otros solo se traen al frente).
- **Cupo de la cuenta**: lo que *queda* de las ventanas de 5 h y 7 d en barras de 10 cuadros, cuenta atrás hasta el reinicio y "PACE" (cuánto de la semana ha pasado). Viene de Claude Code, nunca se inventa; sin datos dice "Capacity unavailable".
- **Permisos y preguntas** (requiere conectar, ver abajo): *Deny / Allow Once / Allow All* para los permisos de herramientas (**Allow All pide una segunda pulsación**, "Confirmar", en 2 s, y solo vale para la sesión en curso), y las preguntas de `AskUserQuestion` (una opción, varias o varias preguntas). El panel se abre solo, crece lo necesario y vuelve a su sitio 1,5 s después de responder.
- Música: título, artista, portada real (Apple Music y Spotify), barra que se arrastra para saltar y controles. Con música sonando el notch cerrado se ensancha con la portada y barras animadas.
- Volumen: cada cambio se muestra en el notch cerrado. Opcionalmente sustituye el HUD de volumen y brillo del sistema (permiso de Accesibilidad).
- Bandeja de archivos (arrastrar y soltar, AirDrop), portapapeles (solo en memoria), snippets, calendario, temporizadores (cuenta atrás, cronómetro, pomodoro), lanzador de apps y espejo con cámara.
- Ajustes (icono de la barra de menús): retraso del hover, corrección del tamaño del notch, abrir al iniciar sesión, conexión con Claude Code, HUD de volumen.
- Vista en vivo de la sesión: texto de Claude con listas (`-`, `1.`), encabezados y código; ediciones con diff por líneas y **palabras cambiadas resaltadas**; el comando de Bash en ejecución con su tiempo, y los comandos terminados plegados en «Ran N shell commands» (pulsa para ver cada comando y el principio de su salida).
- Ajustes con 15 páginas, también **por pantalla** (tamaño y transparencia del notch propios de cada monitor): lanzamiento (Dock, barra de menús, pantalla), apariencia (7 estilos para el inicio, acento, vista previa), notch transparente y vidrio líquido, idioma, tutorial y actualizaciones.
- Atajo global (⌥⌘O por defecto, configurable) para abrir o fijar el panel; opcionalmente ⌥⌘1…9 abren cada pestaña.
- Avisos: notificación de macOS cuando Claude te necesita o una sesión termina, y aviso al llegar a un porcentaje del cupo (70–95 %). El Claude tab dibuja el historial de uso de 5 h y 7 d desde que Caspr lo registra.
- Ajustes: color de acento, pestañas visibles, abrir con clic o con el cursor, retraso al cerrar, velocidad de animación, duración del pomodoro y sonido, formato de hora, temporizador en el notch cerrado y una página de Diagnóstico con "Copiar diagnóstico" (solo estados y recuentos).

---

## 🔌 Conectar con Claude Code

Sin conectar, Caspr ya lee tus sesiones, el cupo y el contexto. Para aprobar permisos y responder preguntas desde el notch hace falta **Ajustes → Claude Code → Conectar**. Antes de tocar nada muestra exactamente qué se añadirá a `~/.claude/settings.json`; guarda una copia de seguridad; solo toca sus propias entradas (reconoce el nombre `notch-ghost-hook`) y *Desconectar* las quita sin tocar lo demás.

Seguridad del puente, comprobada con tests:
- Si Caspr está cerrado, tarda o falla algo, el ayudante responde `{}` y Claude Code usa su aviso normal del terminal: **nunca se aprueba nada por defecto**.
- Socket Unix solo del usuario (carpeta 0700, socket 0600), con token por arranque y comprobación del uid del otro extremo.
- *Allow All* solo vale para la sesión en curso: nunca escribe reglas persistentes ni activa `bypassPermissions`.
- Lo que escribes, las respuestas y las vistas previas de comandos viven solo en memoria.
- Si respondes en el terminal antes que en el notch, la tarjeta desaparece sola.

---

## 🧩 Codex y Cursor

Caspr también puede **observar** Codex y Cursor, sin aprobar ni rechazar nada por ti. Ve a **Ajustes → Codex** o **Ajustes → Cursor → Conectar…**: antes de escribir muestra exactamente qué se añadirá (`~/.codex/config.toml` o `~/.cursor/hooks.json`), guarda una copia de seguridad y *Desconectar* quita solo sus entradas. Después aparece una pestaña por herramienta junto a la de Claude, con una tarjeta por sesión (proyecto, modelo, si trabaja o terminó, y lo último que respondió), y llegan los avisos "Cursor terminó" / "Codex terminó".

- **Cursor** (IDE y `cursor-agent`): usa los hooks oficiales de Cursor. Solo se enganchan eventos que observan; los que pueden permitir o bloquear acciones (`beforeShellExecution`…) no se tocan, así que los permisos de Cursor siguen siendo suyos. La flecha ↗ abre el proyecto en Cursor.
- **Codex** (CLI y app): usa sus hooks de ciclo de vida (`[[hooks.*]]` y `features.hooks = true`); el bloque va entre marcadores y el resto del `config.toml` no se toca. **Pendiente de probar con un Codex real**: sus campos no están documentados y no estaba instalado donde se desarrolló.
- Sin cupo de uso, feed en vivo ni respuesta desde el notch: esas herramientas no exponen esos datos.

## 🔒 Privacidad

Caspr lee tus sesiones y archivos en tu Mac y **no los envía a ningún servidor**. Las únicas conexiones son: GitHub (comprobar y descargar actualizaciones), la portada de Spotify (la URL que Spotify ya da) y, para canciones de Apple Music en *streaming* (que no entregan su portada al Mac), una consulta a la API pública de iTunes con el título y el artista. Esa última se puede apagar en **Ajustes → General → Buscar portadas en internet**.

---

## 📄 Licencia

© 2026 Crisbanks. Todos los derechos reservados. Caspr es de uso gratuito y personal; el código fuente no es público y no se permite redistribuir la app ni hacer ingeniería inversa de ella.

Creado por [Crisbanks](https://github.com/0x-Crisbanks). Este repositorio solo contiene las versiones compiladas y su documentación; las incidencias y sugerencias se abren en [Issues](https://github.com/0x-Crisbanks/Caspr/issues).
