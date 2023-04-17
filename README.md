# Dailys Working - Yuhmak

12-04-2023 <br/>
Conocí la estructura de proyecto tanto en front como back, me tome el tiempo de profundizar en PHP para aportar mucho más a futuro, y se llevo a cabo la realización del botón que va a llevar a la parte en la que se va a ingresar el código del producto a buscar en los productos del hogar y electrodomesticos.

13-04-2023 <br/>
Se realizo la ruta en el back de Node/Express para buscar el producto del hogar que se desee encontrar, y de parte de front se realizo la lógica necesaria para realizar ese pedido al back. Se comprobo dicha funcionalidad y esta andando correctamente. 

14-04-2023 <br/>
Se termino la tabla en la que se renderiza el producto buscado, y además de eso, se llevo a cabo el desarrollo de lo visual sobre donde va an a ir los datos extras y donde podremos sobrescribirlos a futuro.

15-04-2023 <br/>
Se empieza con algunos rediseños para que el uso de la página sea más interactivo y más ameno.

16-04-2023 | 17-04-2023 <br/>
Testeo de bugs de lo anteriormente implementado desde antes que ingrese a Yuhmak. 
Se soluciono los siguientes bugs:<br/>
-Si se da en status de llamada cerrado, el front explotan (solucionado).<br/>
-Devolver una respuesta en caso de no encontrar producto por codigo, dni o chasis. (solucionado).<br/>
Se descubrio los siguientes:
-Si se le da un service a una moto/interno, el mismo service es dado a todas las motos (desconozco si es problema solo de front, testear en back).<br/>
-Al cerrar un service este sigue figurando como abierto en el HomePage (/inicio), y al dar editar llamado al service el back explota (aprender lo más pronto posible SAP para ver el porque de este comportamiento, ya que puede se tanto problema del back de node, como problema de la base de datos SAP).<br/>
-La tarjeta de días atrás de services abiertos renderiza 20 días atrás cosa que se hace en el mismo día.<br/>
-Implementar un loader para la carga de información de los formularios y para mejorar el rendimiento y la funcionalidad de la app.<br/>
-En socio de negocios recibe undefined en destino de factura, cosa que estoy seguro que no debe de ser así.<br/>
