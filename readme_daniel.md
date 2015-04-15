Hola Guille, 
                 Se podria usar el patron stategy para el login usando la autenticacion via twitter por ejemplo, pero lo hice 
con nodeJs y ahora ahora no lo hice con .NET. No se si se aplica en .net 
(aca hay un ejemplo https://github.com/jaredhanson/passport-twitter ) . 
Pero lo que tenemos en .NEt es OpenID y OAuth, entonces podriamos aplicar OAuth para acceder mediante nuestro
login, ya sea con el user cargado en MongoDB o con unos links/botones para poder accer por twitter 
(o facebook/google, o todos).
Por ejemplo habria que ir a https://dev.twitter.com y registrar nuestra aplicacion para generar la relacion de confianza, 
que nos del el access token para poder usarlo en nuesta app. Pero commo dijiste, es bastante trabajoso aplicar esto.

Otras mejoras puede ser:

1) que no permita ingresar un comment en blanco
2) corregir el max length de entrada del texto, que en lugar de 140 char permite infinitos
3) corregir el error si el mail al loguearse esta en blanco o con email invalido porque devuelve null
4) agregar validaciones a los campos de email y password
5) corregir el mensaje de "-x minutes ago" cuando se postea un mensaje, porque esta poniendo cualquier cosa
6) agregar un pequeño test como sugeriste
7) cuando enviamos tags como ser <strong>Hola</strong> que no explote asi: A potentially dangerous request.form value was detected from the client (commentText="<strong>Hola</strong>")
(habilitar en posteo de tags html pero validarlos con alguna sentencia de tipo HTMLenconde y decode.   
8) limitar los rows a mostrar en la grilla o poner un paginador

Por ahora no se me ocurre mas, pero creo que es bastante por el momento

Cuando tenga un hueco de tiempo en mi trabajo me pongo a aplicar algunas mejoras y luego las envio.
Salu2,


Daniel F. Rodríguez
Team Leader - Sr. Develper .NET & SQL server
