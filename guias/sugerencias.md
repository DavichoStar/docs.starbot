# Sugerencias

### Estableciendo el canal 

Para establece el canal en donde se enviaran las sugerencias usa el siguiente comando `sb!set sugerencias <#canal>` 

![Respuesta al usar el comando](../.gitbook/assets/image%20%286%29.png)

### Sugerir

 Envía una sugerencia al servidor con`sb!sugerencia <sugerencia>` 

Al mandar el comando, este se eliminará y mandará una respuesta que también será eliminado en los próximos segundos

![Respuesta al sugerir](../.gitbook/assets/image%20%283%29.png)

La sugerencia se enviara al canal establecido anteriormente para que los usuarios puedan votar

![Los votos no cuenta la reacci&#xF3;n del propio bot](../.gitbook/assets/image%20%281%29.png)

### `Califica las sugerencias`

Tienes tres comandos para aprobar, denegar o indicar como sugerencia potencial:  
Aprueba una sugerencia.  `sb!aprobar <ID> <razón>` 

![Sugerencia aprobada](../.gitbook/assets/image.png)

Pon en potencial una sugerencia. `sb!potencial <ID> <razón>`

![](../.gitbook/assets/image%20%285%29.png)

Rechaza una sugerencia. `sb!rechazar <ID> <razón>`

{% hint style="info" %}
`Los votos son mostrados en el momento que fué usado algún comando de calificación de la sugerecnia, los votos posteriores a eso no serán sumados o restados a los anteriores.`
{% endhint %}
