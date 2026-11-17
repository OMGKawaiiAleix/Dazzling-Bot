# Política de Privacidad

**Última actualización: 11-17-2026**

*Este documento es una traducción del Privacy Policy original en inglés, ofrecida por comodidad. En caso de cualquier discrepancia, prevalece la versión en inglés.*

Esta Política de Privacidad explica cómo Dazzling ("Dazzling", "el bot", "nosotros") recolecta, usa, almacena y protege información cuando usas Dazzling en Discord o interactúas con su documentación oficial.

Dazzling es desarrollado y operado por un desarrollador individual conocido en Discord como **omgkawaiialeix** ("el Desarrollador"). Para cualquier pregunta sobre esta Política, contáctanos a través de nuestro servidor de soporte oficial en Discord: **https://discord.gg/R3AZpftXTm**.

Al usar Dazzling, también aceptas la [Política de Privacidad](https://discord.com/privacy) y los [Términos de Servicio](https://discord.com/terms) propios de Discord, ya que Dazzling opera completamente dentro de la plataforma de Discord y no puede funcionar sin ella.

---

## 1. Información que Recolectamos

Solo recolectamos la información estrictamente necesaria para que las funciones de Dazzling trabajen. La agrupamos en tres categorías:

### 1.1 Contenido que Tú Creas Directamente

Cuando un administrador de servidor usa comandos como `/embed create`, `/embed edit`, `/config`, o `/partner message`, Dazzling guarda el contenido que esa persona escribe o selecciona, incluyendo:

- El texto y la configuración de embeds personalizados: título, descripción, color, nombre/ícono del autor, texto/ícono del footer, URLs de imagen y miniatura, texto de campos, etiquetas y URLs de botones, y el nombre interno/carpeta usados para organizarlos.
- Qué embed y qué canal están vinculados a las funciones de Bienvenida, Boost, Despedida, o Partner (alianzas).

Este contenido lo escribe voluntariamente el administrador del servidor para configurar el comportamiento del bot. Nosotros no generamos, sugerimos ni alteramos este contenido.

### 1.2 Identificadores de Discord

Para que las funciones anteriores trabajen por servidor y por usuario, guardamos los identificadores propios de Discord ("snowflakes"):

- El ID del servidor (guild) de Discord donde se configura una función.
- El ID del usuario de Discord que creó o es dueño de un embed guardado, o que configuró una función.
- El ID del canal de Discord elegido para una función (ej: dónde se debe enviar un mensaje de bienvenida o una alerta de alianza).
- El idioma de respuesta (español o portugués) que un servidor eligió con `/language`.

**No** guardamos nombres reales, correos electrónicos, números de teléfono, ni direcciones físicas. De entrada, no tenemos acceso a esa información a través de la API de Discord.

### 1.3 Información Procesada Temporalmente (No Almacenada)

Cierta información se lee o se usa por un momento para armar un mensaje, y luego se descarta — nunca se escribe en nuestra base de datos:

- **Información del miembro al momento de un evento**: cuando alguien entra a un servidor (Bienvenida), lo boostea (Boost), se sale de él (Despedida), o pega un link de invitación en un canal de alianzas configurado (Partner), usamos brevemente el nombre de usuario, tag, mención y URL del avatar de esa persona de Discord para llenar los placeholders (ej: `{{user.name}}`) del mensaje que diseñó el administrador del servidor. Esta información se usa solo para armar ese mensaje y se descarta de inmediato después.
- **Contenido de mensajes solo en el canal de "Partner"**: si un administrador de servidor configura un canal con `/partner channel`, Dazzling lee el texto de los mensajes publicados **únicamente en ese canal específico**, solo para detectar si un mensaje contiene un link de invitación de servidor de Discord. Si no se encuentra ningún link, no pasa nada. Si se encuentra uno, Dazzling consulta información pública básica sobre esa invitación (el nombre, ícono y cantidad aproximada de miembros del servidor invitado, obtenidos directamente de Discord) para armar una respuesta automática.
  - Dazzling **no** lee, procesa, ni guarda contenido de mensajes de ningún otro canal, para ningún otro propósito.
  - El texto del mensaje en sí, y el link de invitación que contenía, nunca se guardan en nuestra base de datos ni se escriben en ningún registro.
- **Envío por Webhook**: si un administrador de servidor elige enviar un embed con la opción de Webhook (para mostrar un nombre y/o avatar distinto al del bot), Dazzling crea o reutiliza un webhook de Discord en ese canal para enviar el mensaje. Ese webhook es creado y administrado completamente por Discord; nosotros no guardamos su ID, token, ni ningún dato relacionado en nuestra base de datos.

---

## 2. Cómo Usamos la Información

Usamos la información descrita arriba exclusivamente para:

- Operar las funciones que tú o los administradores de tu servidor configuren (embeds personalizados, mensajes automáticos de Bienvenida/Boost/Despedida, y la detección de links de alianza de Partner).
- Permitir que el dueño de un embed lo encuentre, edite, renombre, mueva, transfiera, o elimine.
- Mantener, depurar y mejorar el funcionamiento de Dazzling.

No usamos tu información para publicidad, generación de perfiles, ni para ningún propósito que no sea operar las funciones del bot.

---

## 3. Cómo Almacenamos la Información

Todos los datos descritos en las Secciones 1.1 y 1.2 se guardan en una base de datos SQLite en la infraestructura de hosting de Dazzling. El acceso a nuestra cuenta de hosting está protegido con autenticación de dos factores, y nuestro proveedor de hosting incluye protección contra DDoS. Aun así, como cualquier servicio en línea, no podemos garantizar seguridad absoluta de los datos almacenados o en tránsito.

La consola de nuestro proveedor de hosting no guarda un historial permanente de logs por defecto, y cualquier log técnico que pueda existir temporalmente en la infraestructura no contiene el contenido de tus mensajes de Discord. Nuestro proveedor de hosting puede borrar logs o copias de seguridad a su propio criterio, particularmente si consumen un espacio de almacenamiento considerable.

---

## 4. Retención y Eliminación de Datos

- Los datos vinculados a un servidor se guardan mientras Dazzling siga siendo miembro de ese servidor, sin una fecha de vencimiento fija.
- **Eliminación automática**: si Dazzling es expulsado de un servidor (o el servidor se elimina), todos los datos asociados a ese servidor — cada embed guardado, configuración de Bienvenida/Boost/Despedida, y configuración de Partner — se **eliminan automática e inmediatamente** de nuestra base de datos. Esto no sucede si un servidor simplemente tiene una caída temporal de Discord; Dazzling solo elimina datos cuando realmente ha dejado el servidor.
- **Eliminación manual**: cualquier usuario puede eliminar sus propios embeds guardados en cualquier momento usando `/embed delete`, sin necesidad de sacar al bot del servidor.
- El contenido de mensajes leído en el canal de alianzas de Partner, y los datos de webhooks (Sección 1.3), nunca se almacenan, así que no hay nada que eliminar ahí.
- **Si Dazzling se descontinúa de forma permanente**, haremos un esfuerzo razonable por eliminar todos los datos restantes dentro de un plazo razonable después de que el Servicio cierre.
- Si quieres que eliminemos algún dato específico y las herramientas de arriba no cubren tu situación, puedes contactarnos a través de nuestro servidor de soporte en Discord y atenderemos tu solicitud.

---

## 5. Compartir Información

No vendemos, alquilamos, ni compartimos tu información con terceros con fines de marketing ni ningún otro propósito. La información solo se intercambia con Discord mismo, ya que es inherentemente necesario para que Dazzling funcione como un bot de Discord, y está sujeta a la propia Política de Privacidad de Discord.

---

## 6. Privacidad de Menores

Dazzling está pensado para usarse de acuerdo con los propios Términos de Servicio de Discord, que exigen que los usuarios cumplan con el requisito mínimo de edad de Discord. No recolectamos información a sabiendas de personas que no cumplan con ese requisito, y confiamos en los propios mecanismos de verificación de edad de Discord.

---

## 7. Tus Derechos

Dependiendo de dónde vivas, puedes tener derechos sobre tus datos personales, incluyendo el derecho a acceder, corregir, o solicitar la eliminación de tu información. Si te encuentras en Colombia, esto incluye los derechos reconocidos bajo la **Ley 1581 de 2012 ("Habeas Data")** y sus decretos reglamentarios. Respetamos estos derechos como se describe en la Sección 4 (eliminación por tu cuenta vía `/embed delete`, o eliminación automática cuando el bot sale de tu servidor). Para cualquier otra solicitud, contáctanos a través de nuestro servidor de soporte en Discord.

---

## 8. Donaciones

Dazzling puede ofrecer una forma de apoyar voluntariamente su desarrollo a través de Patreon. Las donaciones las procesa Patreon por completo, y cualquier información de pago o facturación que proporciones la maneja Patreon bajo su propia Política de Privacidad — nosotros no recibimos ni guardamos tus datos de pago.

---

## 9. Uso Internacional

Dazzling puede usarse por servidores y usuarios de todo el mundo. Al usar Dazzling, entiendes que tu información puede almacenarse y procesarse en infraestructura ubicada en un país distinto al tuyo, y que esta Política y los Términos de Servicio se rigen por las leyes de Colombia (ver nuestros Términos de Servicio).

---

## 10. Dónde Se Publican Estos Documentos

Esta Política de Privacidad y nuestros Términos de Servicio se publican como documentos de texto plano (Markdown) en un repositorio público de GitHub, no como un sitio web dedicado. Si los ves en GitHub, tu visita también está sujeta a la [Declaración de Privacidad de GitHub](https://docs.github.com/site-policy/privacy-policies/github-privacy-statement), que es independiente y está fuera de nuestro control.

---

## 11. Cambios a Esta Política

Podemos actualizar esta Política de Privacidad de vez en cuando, por ejemplo para reflejar nuevas funciones o requisitos legales. Cuando lo hagamos, actualizaremos la fecha de "Última actualización" en la parte superior de esta página. Continuar usando Dazzling después de que los cambios entren en vigor significa que aceptas la Política actualizada.

---

## 12. Contacto

Si tienes alguna pregunta sobre esta Política de Privacidad o sobre cómo se maneja tu información, contacta a **omgkawaiialeix** a través de nuestro servidor de soporte oficial en Discord: **https://discord.gg/R3AZpftXTm**.
