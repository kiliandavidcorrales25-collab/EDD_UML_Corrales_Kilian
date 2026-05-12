# EDD_UML_Corrales_Kilian

## Explicacion del UML
1. Tras la Actividad 1 “Pulsar “Finalizar compra””, se usa un diagrama de flujo, ya que el cliente nos pide que la Actividad 2 y 3  transcurren simultáneamente

2. Para la Actividad 2 y 3 de “Verificar stock” y “Verificar validez de la sesión” se decide usar el modelo de subActividad, haciendo un UML interno, para no sobrecargar el UML principal
   
3. Dentro de la Actividad 2, se comprueba si el “artículo” que quiere comprar el cliente queda en stock, sino es asi, 
lo sacará automáticamente del carrito y se finaliza la compra, si queda stock, continuará
   
4. Dentro de la Actividad 3, se comprobará si el usuario tiene su cuenta iniciada, de no ser así, se le preguntará por sus datos para loguearse, 
si los datos se encuentran en la base de datos continuará al UML principal, y si la sesión es correcta igual, si los datos son incorrectos volverá al paso 3.2 de logueo

6. Si ambos datos de la Actividad 2 y 3 Son correctos se pasará a la ventana de “Finalizar compra”, 
El usuario podrá cancelar y salir de este proceso y terminar el UML, o podrá confirmar la compra y pasar a la pasarela de pago

7. Se le pedirá al usuario los datos de su cuenta bancaria para proceder al pago, 
si los datos son incorrectos se repetirá este proceso hasta que sean correctos, 
cuando sea exitoso se volverá a realizar la estrategia del modelo de subActividad

8. Se realizan de forma simultánea los procesos de Registro del pedido en la base de datos, generación del PDF de la factura 
y envío de notificación al usuario, este último será una subActividad, ya que debe comprobar los datos del usuario logueado en el sistema
Cuando estos 3 proceso acaben se mostrará un mensaje de confirmación y se enviará a la página de compra otra vez, y terminará

## Herramientas usadas 
**Los nodos de si­n­cro­ni­za­ción:** funcionan de unificación para varias transacciones en UML, Se usa cuando varios conexiones entran a la vez, pero sólo uno de ellos puede salir.	[1]

**SubActivad**: Un UML interno al UML principal, que se usa para descargar carga del UML principal y no se vea tan compacto

## Referencias
[1] Diagramas de actividades: el flujo de trabajo representado gráficamente. (2023, marzo 1). ionos Digital Guide. https://www.ionos.es/digitalguide/paginas-web/desarrollo-web/diagramas-de-actividades-uml/ 

