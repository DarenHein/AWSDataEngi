

### CDC (Change data capture)

el _CDC_ es una tecnica de la ingeniria de datos donde movmos informacion de punto a a punto b pero _solamente la infromacion __nueva__ !_ 

## ANALOGIA 

un estudiante cuando falta un dia de clases , pide a su amigo la libreta de matematicas y sacarles fotocopias , en ves de fotocopiar todo el ucaderno de matematicas con infromacion desde que inicio el curso simplemente toma la infomacion del dia que falto 

***Como Funciona el CDC***

en las empresas existen bases de __datos trancsaccionales__ (_OLTP_) donde los clientes estan comprando todo el tiempo nosotros necesitramos llevar esa infomacion a nuestro _data lake_ o a nuestro _data Where house_ 

el cdc se encarga de de vigilar esa base de datos en el mismo segundo que ocurre el sacado de informacion el _CDC_ genera un reporte con 3 eventos 

### EVENTOS CDC :

_1 Insert_ : se creo un nuevo registro (el cdc toma ese registro y lo manda al destino) 

_2 update_ : luis cambio su domicilio (el cdc solo manda el aviso del cambio)

_3 delete_ : Luis cancelo su cuenta (el cdc avisa que se debe de borrar o poner en incativo)