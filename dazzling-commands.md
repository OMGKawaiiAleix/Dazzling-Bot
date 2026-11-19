# 🩷 Dazzling - Comandos y funciones actuales

## `/embed` - Crear y administrar embeds personalizados

- `/embed create` - crea un embed nuevo (nombre + carpeta opcional)
- `/embed list` - lista tus embeds guardados, agrupados por carpeta
- `/embed list-all` - lista los embeds de todos los usuarios del servidor
- `/embed edit` - abre el editor visual de uno de tus embeds
- `/embed edit-other` *(solo Administradores)* - edita el embed de otra persona
- `/embed delete` - elimina un embed (con confirmación)
- `/embed rename` - renombra un embed (actualiza automáticamente botones/vínculos/Bienvenida/Boost/Despedida que lo usaran)
- `/embed folder` - mueve un embed a una carpeta
- `/embed transfer` - transfiere uno de tus embeds (o una carpeta completa) a otro usuario
- `/embed transfer-other` *(solo Administradores)* - fuerza la transferencia del embed de otra persona, sin que ella tenga que hacer nada

### Editor visual (botones)

Editar (título/descripción/color), Texto (fuera del embed), Autor, Footer, Imágenes, Botones (de enlace o que muestran otros embeds), Vincular embed, Renombrar, Vista previa, Enviar aquí, Otro canal, Webhook (nombre/avatar personalizado), Cancelar.

### Placeholders disponibles

- `{{user.mention}}`, `{{user.name}}`, `{{user.tag}}`, `{{user.id}}`, `{{user.avatar}}`, `{{user.memberNumber}}`
- `{{server.name}}`, `{{server.members}}`, `{{server.icon}}`, `{{server.boosts}}`
- `{{partner.name}}`, `{{partner.icon}}`, `{{partner.members}}`, `{{partner.link}}`, `{{partner.count}}`

---

## `/config` - Mensajes automáticos del servidor

- `/config welcome` - mensaje de bienvenida (embed + canal)
- `/config boost` - mensaje cuando alguien boostea
- `/config goodbye` - mensaje cuando alguien se va del servidor
- `/config disable` - apaga uno de los tres

---

## `/partner` - Alianzas con otros servidores

- `/partner channel` - canal donde se detectan automáticamente los links de invitación de Discord
- `/partner message` - tu propio embed de respuesta (o el diseño por defecto si no configuras ninguno)
- Lleva la cuenta de cuántas alianzas ha hecho cada persona (`{{partner.count}}`)

---

## `/autorole` - Asignación automática de rol por texto

Un solo comando, todo opcional (deja vacío para ver el estado actual):

- `channel`, `text`, `give_role`, `remove_role` - canal, texto gatillo exacto, rol que asigna, rol que quita (opcional)
- `confirm_text` / `confirm_embed` / `confirm_disabled` - cómo se confirma (texto propio, un embed guardado, o nada)
- `delay` - segundos para que la confirmación se borre sola (0 = nunca)
- `delete_trigger` - si también borra el mensaje de quien escribió el texto
- `disable` - apaga todo

Muestra un embed de estado tipo panel (✅/❌ por cada campo).

---

## `/language` - Idioma de respuestas

Español o Português - afecta todo lo que dice el bot (confirmaciones, errores, `/help`), excepto nombres de comandos y placeholders, que siempre quedan en inglés.

---

## `/help` - Ayuda categorizada

Menú desplegable con: Embeds, Configuración del servidor, Partner, Auto-Rol.

---

## Protecciones y comportamiento de fondo

- **Permisos:** todos los comandos (excepto `/help`) requieren "Gestionar Servidor". `/embed edit-other` y `/embed transfer-other` piden además Administrador completo.
- **Cooldowns:** 3 segundos entre usos del mismo comando por persona; 4 segundos por servidor para la detección de Partner.
- **Aislamiento de datos:** cada servidor tiene su información completamente separada.
- **Borrado automático:** si sacan a Dazzling de un servidor, todos sus datos de ese servidor se eliminan al instante (embeds, configuraciones, Partner, Auto-Rol).
- **Privacidad:** no guarda contenido de mensajes fuera del canal de Partner, ni datos de webhooks (los crea Discord, Dazzling no los almacena).
