
# VENTANAS DE TIEMPO (TIME WINDOWS)

primero entender como fluyen los datos los datos nunca se detienen son un rio continuo y infinito para poder aplicar operaciones en este rio de datos que _nunca_ se detiene ocupamos las _ventanas de timepo_ para verlas en analogia vendrian siendo _cubetas_ que tomamos pedacitos de agua(datos) y aplicamos nuestras operaciones matematicas en el agua(datos) que estan dentro de la cubeta(_ventanas_)

### _Tipos de Ventanas_

1- _VENTANA FIJA O DE SALTO_ __(TUMBLING WINDOW)__

_tipo de ventana_ : "ventanas disjuntas" -> que no se mexclan una de las otras  

__Analogia__

seguimos con la anlogia del rio infinito de datos el _tumbling window_ son cubetas apiladas una tras de otra con un intervalo de tiempo cada unoa osea , cada cubeta apilada tiene 5 minutos de vida lso datos que lleguen a esa cubeta en ese lapso de tiempo y fin y sigue la otra con el mismo lapso de tiempo 