---
description: >-
  Aquí aprenderás sobre cómo funciona el archivo de configuración y, en las
  siguientes páginas, cómo configurarlo todo.
---

# Introducción

Primero debes de tener permiso de Administrador para usar el comando `/config export`, éste te mandará un archivo con la configuración actual. _(Opcionalmente puedes usar el parámetro template para que te dé una plantilla con la configuración de ejemplo básica o completa que se puede hacer al bot)._

{% hint style="info" %}
Recomendamos utilizar un editor de texto como Visual Studio Code o Notepad++ para abrir el archivo, puedes utilizar el que más te guste, incluso el bloc de notas de Windows.
{% endhint %}

Puede ser muy diferente su archivo, pero si es la primera vez que lo utiliza, se debe de parecer a este:

{% code title="config.yml" %}
```yaml
# |============================================|
# |                  StarLigh                  |
# |    Soporte: https://discord.gg/VG6D4ss     |
# |              Plantilla Básica              |
# |============================================|

# Color personalizado
colorMain: '#13b9c4'

# Idioma
language:
  # Idiomas dimerentes en canales en específico.
  channels:
    - id: "518210945185611830"
      language: en-US
      
# Sistemas de bienvenidas.
welcome:
    # Roles que se le asignará a nuevos miembros.
    roles: ['123456789012345678']
    # Imagen autogenerada de bienvenida.
    image:
        # Id del canal donde se enviará.
        channel: '123456789012345678'
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
```
{% endcode %}

{% hint style="info" %}
Todo lo que está después del signo de gato (**#**) Es un comentario, esto no afectará en lo más mínimo en tu configuración. Pero después de subido se eliminará cuando vuelvas a solicitar tu configuración.
{% endhint %}

Más adelante verás cómo configurar cada parte de este archivo.

Para aplicar los cambios, solamente debes de ejecutar el comando `/config import` con el archivo modificado en el parámetro de `file`.

{% hint style="danger" %}
Para eliminar una configuración, solamente debes de quitar TODOS los parámetros que correspondan o que sean opcionales. Después de eliminado, no se puede recuperar al menos que suba de nuevo el archivo anterior.
{% endhint %}
