# Bienvenida

## Auto-Rol/es de Entrada

Para usarlo, necesitas poner `roles` Los parámetros que espera es el rol.

```yaml
welcome:
    roles: ['123456789012345678', '123456789012345678']
```

Otra manera de poner esto mismo es:

```yaml
welcome:
    roles:
        - '123456789012345678'
        - '123456789012345678'
```

{% hint style="info" %}
Si no sabes cómo sacar el ID de un rol, [ve esta información.](../preguntas-frecuentes.md#como-saco-un-id-de-un-canal-rol-o-usuario)
{% endhint %}

## Estilo Embed

Para configurar, necesitas poner `embed` de la siguiente manera: &#x20;

```yaml
welcome:
        embed:
                # Id del canal donde se enviará.
                channel: '123456789012345678'
        
                # Mensaje que se mandará junto al embed.
                message: ¡Hola {user}! Bienvenido a esta comunidad # Propiedad Opcional
        
                # Mensaje que estará en la descripción del embed.
                message_embed: 'Que te la pases bien en este servidor :star:' # Propiedad Opcional
        
                # Imagen del embed.
                image: 'https://pagina.com/imagen.gif' # Propiedad Opcional
```

{% hint style="info" %}
En este y otros parámetros que lleven un mensaje, las propiedades que acepta como marcadores (tipo `{user}`), las puedes consultar [aquí](../preguntas-frecuentes.md#cuales-son-los-marcadores-de-posicion-que-puedo-usar-en-los-mensajes-de-los-comandos).
{% endhint %}

Esto es un ejemplo de cómo se vería el resultado:&#x20;

![¡Hola {user} Bienvenido a esta armada!](<../.gitbook/assets/image (9).png>)

## **Estilo Imagen**

Con la propiedad `image` es con la que podemos usar este estilo.

```yaml
welcome:
    image:
        # Id del canal donde se enviará.
        channel: '123456789012345678'

        # Mensaje que se mandará junto a la imagen.
        message: 'Denle la bienvenida a {user_name} eres el miembro #{server_members}' # Propiedad Opcional

        # Mensaje corto de la imagen.
        image_message: Acaba de aterrizar un nuevo miembro ¡Saluden! # Propiedad Opcional

        # Array de fondos que se mandarán de forma aleatoria.
        background:
            # Enlace de la imagen.
            - url: 'https://pagina.com/imagen.gif'

            # Colores para usar en la imagen.
            colors:  # Propiedad Opcional

                # Color principal de los páneles.
                main: '#13b9c4'

                # Color secundario del panel inferior.
                secondary: '#212121'

                # Color del texto.
                text: '#fff'

                # Color del texto secundario.
                text_secondary: '#fff'

            # Opción dos
            - url: 'https://pagina.com/imagen.gif'
            colors:
                main: '#13b9c4'
                secondary: '#000000'
                text: '#ffffff'
```

Aquí tenemos muchas opciones, las primeras ya las conoces, pero la propiedad `message` es para el mensaje que se mandará junto a la imagen, mientras `image_message` es el mensaje corto que se mandará dentro de la imagen.

En la propiedad de `background` se pone la imagen y los colores: `url` el enlace de una imagen válida terminada en .png, .jpg o .gif (Aunque no tendrá movimiento), en la propiedad `colors` tenemos 4 propiedades:

* main: es el color que se le da a la línea de la izquierda, el contorno de la foto de perfil y en la palabra **Biendenid@ a** en este caso es un color azul.
* secondary: Es el color del nombre del servidor y el mensaje, en este caso gris oscuro.
* text: Es el color que se le da a todo el texto en lo que corresponde al color main (azul), en este caso es blanco.
* text\_secondary: Es el color del texto que corresponde al color secondary (gris oscuro), igualmente en este caso es blanco.

![Ejemplo.](<../.gitbook/assets/image (10).png>)

{% hint style="warning" %}
Es probable que los caracteres especiales poco comunes y emojis no salgan bien o de la manera esperada. Incluso puede salir un cuadrado ⬜  en su lugar.
{% endhint %}

{% hint style="info" %}
Si lo notaste, en la propiedad de `background` se puede colocar más de un fondo con sus colores, esta es una función exclusiva de la suscripción premium del bot. Más información [`aquí`](../#apoyar-al-bot).
{% endhint %}

## Apodo Inicial

Con la propiedad `nickname` puedes colocar un emoji o prefijo al nombre de un usuario recién que entra al servidor, como por ejemp**l**o: **⭐ DavichoStar**

```yaml
welcome:
    nickname: '⭐'
```

## Registro de Entrada

Con la propiedad `channel_entry` pero de la propiedad padre `logs` se puede establecer el canal de los registros donde un usuario al entrar se mostrará su tiempo de creación de la cuenta.

```yaml
logs:
    channel_entry: '123456789012345678'
```

{% hint style="info" %}
En la suscripción premium, trata de darte la invitación probable con la que entró este usuario. Estamos trabajando constantemente para que esto sea 100% precisa.
{% endhint %}
