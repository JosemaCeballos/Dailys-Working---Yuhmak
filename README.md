# Dailys Working - Yuhmak

12-04-2023 <br/>
Conocí la estructura de proyecto tanto en front como back, me tome el tiempo de profundizar en PHP para aportar mucho más a futuro, y se llevo a cabo la realización de la ruta y del botón que va a llevar a la parte en la que se va a ingresar el código del producto a buscar en los productos del hogar y electrodomesticos.<br/>
App:<br/>
![image](https://user-images.githubusercontent.com/109984981/233095043-865504b0-06ef-4afe-8aa6-740672745e50.png)
page/HomePage:<br/>
![image](https://user-images.githubusercontent.com/109984981/233095790-7ac38e96-f003-482f-9072-5701c76386e7.png)
page/ClientPage:<br/>
Además también se mejoro la lógica para renderizar una página u otra de manera tal que si a futuro se desea agregar nuevas rutas, estas puedan ser agregadas fácilmente:<br/>
![image](https://user-images.githubusercontent.com/109984981/233095524-dbc4ba80-7303-4d14-a4fb-619ba1c3758f.png)


13-04-2023 <br/>
Se realizo la ruta en el back de Node/Express para buscar el producto del hogar que se desee encontrar, y de parte de front se realizo la lógica necesaria para realizar ese pedido al back. Se comprobo dicha funcionalidad y esta andando correctamente. 

14-04-2023 <br/>
Se termino la tabla en la que se renderiza el producto buscado, y además de eso, se llevo a cabo el desarrollo de lo visual sobre donde va an a ir los datos extras y donde podremos sobrescribirlos a futuro.

15-04-2023 <br/>
Se empieza con algunos rediseños para que el uso de la página sea más interactivo y más ameno.

16-04-2023 | 17-04-2023 <br/>
Testeo de bugs de lo anteriormente implementado desde antes que ingrese a Yuhmak. 
Se soluciono los siguientes bugs:<br/>
-Si se da en status de llamada cerrado, el front explota (solucionado).<br/>
-Devolver una respuesta en caso de no encontrar producto por codigo, dni o chasis. (solucionado).<br/>
Se descubrio los siguientes:<br/>
-Si se le da un service a una moto/interno, el mismo service es dado a todas las motos (desconozco si es problema solo de front, testear en back).<br/>
-Al cerrar un service este sigue figurando como abierto en el HomePage (/inicio), y al dar editar llamado al service el back explota (aprender lo más pronto posible SAP para ver el porque de este comportamiento, ya que puede se tanto problema del back de node, como problema de la base de datos SAP).<br/>
-La tarjeta de días atrás de services abiertos renderiza 20 días atrás cosa que se hace en el mismo día.<br/>
-Implementar un loader para la carga de información de los formularios y para mejorar el rendimiento y la funcionalidad de la app.<br/>
-En socio de negocios recibe undefined en destino de factura, cosa que estoy seguro que no debe de ser así.<br/>

17-04-2023<br/>
Decidi crear mis componentes de 0, deje creado el guardado de información dentro de un objeto.<br/>

18-04-2023<br/>
Estructure completamente el contenido de los componentes de HomeAppliances de manera tal que si cualquiera quiere agarrar el código lo pueda entender de manera sencilla o recibiendo explicaciones muy basicas.Hice pequeñas correcciones al guardado de la información para que este tenga un funcionamiento mas apto para lo necesario, valide dicho formulario de manera tal que solo me falte recibir el endpoint del back y mande la información (también se aplico la lógica para mandar dicha información de manera tal que si no cumple con las validaciones la información no sea mandada, y en caso de cumplir con lo exigido la envie. <br/>

19-04-2034 <br/>
Se tiene la intención de avanzar con el arreglo de los bugs, creo que la sección renderizado de servicio va a tener que ser realizada completamente aparte del formulario, aún tengo esa duda en standby.
