---
description: Cómo configurar correctamente el idioma en tu servidor.
---

# Idioma

Para establecer el idioma principal de todo el bot, existe la propiedad `server`, pero esta propiedad desaparecerá o será ignorado en el futuro, ya que el bot tomará el idioma establecido en el servidor.

```yaml
language:
    server: es-MX
```

Las opciones que se pueden usar son: <mark style="color:blue;">en-US</mark>, <mark style="color:green;"></mark> <mark style="color:blue;">es-AR</mark>, <mark style="color:blue;">es-ES</mark>, <mark style="color:blue;">es-MX</mark>, <mark style="color:blue;">pt-BR</mark>. Pero el idioma principal y por defecto es es-MX, esto quiere decir que los demás idiomas pueden tener errores o estar incompletos. Si quieres ayudar en la traducción, te invito a preguntar en el [servidor de soporte](../soporte.md).

```yaml
language:
    channels:
        - id: '123456789012345678' # Id del canal de discord.
        language: en-US # Idioma del canal.
        # Otro canal
        - id: '123456789012345678'
        language: es-ES
```

Para personalizar aún más el bot, puede escoger un idioma específico para un canal colocándolo en esta propiedad `channels` _(cada **-** es un canal a configurar)_ entonces en la propiedad `id` colocarás el ID del canal de texto, en la propiedad `language` será el idioma que se usará en ese canal.

{% hint style="info" %}
Si no sabes cómo sacar el ID de un canal, [ve esta información.](../preguntas-frecuentes.md#como-saco-un-id-de-un-canal-rol-o-usuario)
{% endhint %}
