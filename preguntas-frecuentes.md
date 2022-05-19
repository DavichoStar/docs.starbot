---
description: Dudas que comúnmente nos hacen o son constantes en distintas comunidades.
---

# Preguntas Frecuentes

## ¿Puedo invitar a StarLight a mi servidor?

¡Claro! eres libre de meterlo a todas partes y rincones de Discord\
Solamente [Entra Aquí](https://discord.com/oauth2/authorize?client\_id=517786947171909643\&permissions=8\&scope=bot%20applications.commands) para invitarlo.

## ¿Cuáles son los marcadores de posición que puedo usar en los mensajes de los comandos?

Un marcador de posición se refiere a que en un mensaje tenemos `¡Hola {user]!` Ese **user** puede ser una persona diferente dependiendo de quién use el comando o provoque un evento. Pero no es el único, los siguientes son los disponibles:



* **{user}** Hace una mención del usuario **(En los mensajes en imágenes no se puede usar este marcador).**
* **{user\_name}** Coloca el nombre de usuario como texto simple.
* **{user\_nickname}** Coloca el apodo (Si tiene uno) del usuario en el servidor.
* **{user\_tag}** Coloca el nombre, el signo # y los 4 número de su nombre de usuario de Discord.
* **{user\_id}** Colocar el Identificador Único (ID) del usuario.
* **{server\_name}** Coloca el nombre del servidor actual.
* **{server\_id}** Coloca el Identificador Único (ID) del servidor.
* **{server\_members}** Coloca el número de miembros en el servidor actualmente (Ya sean usuarios o bots).
* **{server\_created}** Coloca la fecha de creación del servidor.
* **{server\_created\_timestamp}** Coloca la fecha de creación del servidor con marca de tiempo, ejemplo: `hace 3 años`

## ¿Cómo saco un ID de un canal, rol o usuario?

Para esto, debes de ir a `Ajustes de Discord > Avanzado > Modo desarrollador` y activarlo.

![Activar Modo desarrollador](.gitbook/assets/Settings)

Tendiendo esto activado ahora puedes dar click derecho en lo que necesites, un mensaje, un rol, un usuario o un canal y aparecerá la opción `Copiar ID`, le das click y listo! Ya tienes su Identificador Único.

![ID de un usuario](<.gitbook/assets/User ID>) ![ID de un canal](<.gitbook/assets/Channel ID>) ![ID de un rol](<.gitbook/assets/Role ID>)

## ¿Cómo puedo ver las configuraciones que tengo?

Para saber todos los  ajustes que se han puesto en tu servidor, debe de ejecutar `/config export` y te mandará un archivo YAML con toda tu configuraciones desde las bienvenidas hasta los roles por nivel.

## ¿Por qué no me responde StarLight?

Si eres veterano de Discord, tal vez estés acostumbrado a usar prefijos. Ahora se usan con `/` de este y otros bots, sólo busca la foto del bot en la lista que se abrirá, pero si sigue sin responder, verifica lo siguiente:

1. Deberías verificar que esté conectado StarLight.
2. Revisa que tenga permisos de escribir, preferiblemente que tenga el permisos de Administrador para no tener conflictos con varios comandos de Moderación.
3. También tienes que verificar, si un comando es el que no responde, que no esté desactivado este comando dentro del servidor, pero siempre te mandará un aviso si es que está desactivado.
4. Si aún así no funciona, contacta con nosotros en el [Servidor de Soporte](soporte.md)

