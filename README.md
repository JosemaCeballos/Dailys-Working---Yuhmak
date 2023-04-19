# Dailys Working - Yuhmak

12-04-2023 <br/>
Conocí la estructura de proyecto tanto en front como back, me tome el tiempo de profundizar en PHP para aportar mucho más a futuro, y se llevo a cabo la realización de la ruta y del botón que va a llevar a la parte en la que se va a ingresar el código del producto a buscar en los productos del hogar y electrodomesticos.<br/>
App:<br/>
![image](https://user-images.githubusercontent.com/109984981/233095043-865504b0-06ef-4afe-8aa6-740672745e50.png)<br/>
page/HomePage:<br/>
![image](https://user-images.githubusercontent.com/109984981/233095790-7ac38e96-f003-482f-9072-5701c76386e7.png)<br/>
page/ClientPage:<br/>
Además también se mejoro la lógica para renderizar una página u otra de manera tal que si a futuro se desea agregar nuevas rutas, estas puedan ser agregadas fácilmente:<br/>
![image](https://user-images.githubusercontent.com/109984981/233095524-dbc4ba80-7303-4d14-a4fb-619ba1c3758f.png)<br/>
![image](https://user-images.githubusercontent.com/109984981/233096318-4d1b5d6d-c041-400e-bf95-a7dccc06e708.png)<br/>



13-04-2023 <br/>
Se realizo la ruta en el back de Node/Express para buscar el producto del hogar que se desee encontrar, y de parte de front se realizo la lógica necesaria para realizar ese pedido al back. Se comprobo dicha funcionalidad y esta andando correctamente. <br/>
Backend:<br/>
![image](https://user-images.githubusercontent.com/109984981/233096552-e713149c-20b8-4488-b778-958222f04209.png)<br/>
Frontend (realizado utilizando puro contexto global -/contexts/homeApplianceContext/index.js-):<br/>
![image](https://user-images.githubusercontent.com/109984981/233096940-764127be-412e-445a-a932-20e52824f896.png)<br/>


14-04-2023 <br/>
Se termino la tabla en la que se renderiza el producto buscado, y además de eso, se llevo a cabo el desarrollo de lo visual sobre donde va a ir los datos extras y donde podremos sobrescribirlos a futuro. <br/>
![image](https://user-images.githubusercontent.com/109984981/233097419-a1847680-a3f9-49a3-8785-54d3fd4128a9.png) <br/>

15-04-2023 <br/>
Se empieza con algunos rediseños para que el uso de la página sea más interactivo y más ameno.<br/>
![image](https://user-images.githubusercontent.com/109984981/233098051-d454ad4c-0e12-46f8-ad29-b674629e9117.png) <br/>

16-04-2023 | 17-04-2023 <br/>
Testeo de bugs de lo anteriormente implementado desde antes que ingrese a Yuhmak. 
Se soluciono los siguientes bugs:<br/>
-Si se da en status de llamada cerrado, el front explota (solucionado).<br/>
-Devolver una respuesta en caso de no encontrar producto por codigo, dni o chasis. (solucionado).<br/>
Se descubrio los siguientes:<br/>
-Si se le da un service a una moto/interno, el mismo service es dado a todas las motos (desconozco si es problema solo de front, testear en back).<br/>
-Al cerrar un service este sigue figurando como abierto en el HomePage (/inicio), y al dar editar llamado al service el back explota (aprender lo más pronto posible SAP para ver el porque de este comportamiento, ya que puede se tanto problema del back de node, como problema de la base de datos SAP).<br/>
-La tarjeta de días atrás de services abiertos renderiza 20 días atrás cosa que se hace en el mismo día.<br/>
-En socio de negocios recibe undefined en destino de factura, cosa que estoy seguro que no debe de ser así.<br/>

17-04-2023<br/>
Decidi crear mis componentes de 0, de manear tal que toda la información necesaria se guarde dentro de un objeto y a futuro reciba modificaciones minimas.<br/>

18-04-2023<br/>
Estructure completamente el contenido de los componentes de HomeAppliances de manera tal que si cualquiera quiere agarrar el código lo pueda entender de manera sencilla o recibiendo explicaciones muy basicas.Hice pequeñas correcciones al guardado de la información para que este tenga un funcionamiento mas apto para lo necesario, valide dicho formulario de manera tal que solo me falte recibir el endpoint del back y mande la información (también se aplico la lógica para mandar dicha información de manera tal que si no cumple con las validaciones la información no sea mandada, y en caso de cumplir con lo exigido la envie. <br/>
Organización de carpetas para homeAppliances: <br/>
-FormService contiene el formulario en el que se renderiza información extra y donde se guarda la información dentro de un objeto. InputServices contiene la información extra, Senders contiene lo que se modifica, y TabsMenu contiene lo renderizado según la sección deseada.)<br/>
![image](https://user-images.githubusercontent.com/109984981/233098982-bd496210-acdc-4e6d-bdb1-262e8fd6bf08.png)<br/>
-Service contiene las funciones que les pegan a un endpoint <br/>
-HomeApplianceInput contiene la barra de busqueda según el código del producto <br/>
-TableOfHomeAppliance contiene la tabla que primeramente se renderiza una vez la busqueda es realizada <br/>
Validación de información en el context: <br/>
![image](https://user-images.githubusercontent.com/109984981/233100163-ad73a22e-4ea7-4df0-b5f4-6643f6ff7602.png)
Context de homeAppliance: <br/>
-Dentro de la carpeta controllers de momento se encuentra la validación, a futuro va a estar las nuevas funciones que se deban realizar y aplicar sobre mi estado global.<br/>
-index.js contiene todo lo necesario para que mi contexto global funcione de manear correcta y sea lo más legible e entendible posible.<br/>


19-04-2034 <br/>
Se tiene la intención de avanzar con el arreglo de los bugs, creo que la sección renderizado de servicio va a tener que ser realizada completamente aparte del formulario, aún tengo esa duda en standby.
Bugs slucionados:<br/>
-Al cerrar un service este sigue figurando como abierto en el HomePage (/inicio), y al dar editar llamado al service el back explota (aprender lo más pronto posible SAP para ver el porque de este comportamiento, ya que puede se tanto problema del back de node, como problema de la base de datos SAP).<br/>
-Si se le da un service a una moto/interno, el mismo service es dado a todas las motos/interno (el problema era de front, se soluciono a través de un condicional que si la ruta contiene "servicio-interno" renderice una cosa u otra. A futuro SI o SI se debera hacer un nuevo formulario para renderizar la información del servicio especifico.<br/>
-En socio de negocios recibe undefined en destino de factura, cosa que estoy seguro que no debe de ser así. Con respecto a esto se decidio no renderizarlo en servicio interno ya que la dirección solo es necesaria cuando se recibe de los clientes.

