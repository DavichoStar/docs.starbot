---
description: >-
  Aprende a configurar los parámetros para que al ingresar un nuevo usuario a tu
  servidor, este lo reciba con un bonito mensaje o imagen. O si es que se
  retira, que no pase desapercibido por los demás.
---

# Bienvenidas/Despedidas

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

## Mensajes Aleatorios

SI buscas algo sencillo pero genial, puedes personalizar distintos mensajes que se mandarán aleatoriamente, a este le puedes sumar los marcadores de posición y ya tienes mensajes al estilo Discord pero personalizados.

{% hint style="info" %}
En este y otros parámetros que lleven un mensaje, las propiedades que acepta como marcadores (tipo `{user}`), las puedes consultar [aquí](../preguntas-frecuentes.md#cuales-son-los-marcadores-de-posicion-que-puedo-usar-en-los-mensajes-de-los-comandos).
{% endhint %}

Este se configura con el parámetro `random_message` como a continuación:

```yaml
random_message:
    # Id del canal donde se enviará.
    channel: '123456789012345678'
    # Lista de mensajes a enviar aleatoriamente.
    messages:
        - "Llegó {user_name} a sorprender a todos"
        - "Tenemos a un nuevo miembro, su nombre es {user_name}"
        - "¡Vengan todos a saludar a {user}!"
        - "Todos de pie que está entrando {user} al servidor"

```

El parámetro `channel` requiere un ID de 18 dígitos del canal y `messages` recibe una lista de los mensajes que tendrá disponibles para mandar.

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
                images: ['https://pagina.com/imagen.gif', 'https://pagina.com/imagen.gif'] # Propiedad Opcional
```

El parámetro `channel` recibe el id de un canal, `message` será el que mandará junto al mensaje, este puede mencionar al usuario si ponemos `{user}`. `message_embed` es un mensaje que va dentro del embed que no hace ping de las menciones que se hagan dentro. Por último tenemos a `images`, que recibe una lista de urls de imágenes.

Esto es un ejemplo de cómo se vería el resultado sin imágenes:&#x20;

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
        image_message: 'Acaba de aterrizar un nuevo miembro ¡Saluden!' # Propiedad Opcional

        # Tema de la distribución o apariencia de la imagen. Por ejemplo: default, classic o center
        # servidor premium tiene más opciones, revisa el comando /premium info
        theme: 'default' # Propiedad Opcional

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

La propiedad `theme` sirve para cambiar la apariencia y distribución de la image, esto quiere decir que hay tres opciones de distribución y hay varias opciones de apariencia para usuario que mejoren el servidor con su suscripción premium, como por ejemplo neon\_center o retro\_wave. Consulta el comando premium para más información.

En la propiedad de `background` se pone la imagen y los colores: `url` el enlace de una imagen válida terminada en .png, .jpg o .gif (Aunque no tendrá movimiento), en la propiedad `colors` tenemos 4 propiedades:

* main: es el color que se le da a la línea de la izquierda, el contorno de la foto de perfil y en la palabra **Biendenid@ a** en este caso es un color azul.
* secondary: Es el color del nombre del servidor y el mensaje, en este caso gris oscuro.
* text: Es el color que se le da a todo el texto en lo que corresponde al color main (azul), en este caso es blanco.
* text\_secondary: Es el color del texto que corresponde al color secondary (gris oscuro), igualmente en este caso es blanco.

![Ejemplo de classic](<../.gitbook/assets/image (10).png>) ![Ejemplo de neon\_center](<../.gitbook/assets/Ejemplo Welcome 2.png>) ![Ejemplo de retro\_wave](<../.gitbook/assets/Ejemplo Welcome 3.png>)

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

![Ejemplo con invitación usada](<../.gitbook/assets/image (11).png>)

{% hint style="info" %}
En la suscripción premium, trata de darte la invitación probable con la que entró este usuario. Estamos trabajando constantemente para que esto sea 100% precisa.
{% endhint %}

## Despedidas

Ahora te preguntarás ¿Cómo se configuran las despedidas? Bueno pues es exactamente igual que todo lo anterior, cambiando `welcome` por `leave` y exceptuando los apartados de **Auto-Role, Apodo Inicial y Registro de Entrada**. Por ejemplo para embed sería:

```yaml
leave:
    # Mensaje tipo embed.
    embed:
        # Id del canal donde se enviará.
        channel: '123456789012345678'

        # Mensaje que se mandará junto al embed.
        message: Se nos fue de {server_name} otro usuario # Propiedad Opcional

        # Mensaje que estará en la descripción del embed.
        message_embed: Nos vemos pronto # Propiedad Opcional

        # Imagenes del embed. | Puedes poner más de un enlace si tienes el servidor
        #                       mejorado con premium
        images: ['https://pagina.com/imagen.gif', 'https://pagina.com/imagen2.gif'] # Propiedad Opcional
```
