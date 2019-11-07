# JQuery
1. [Instalación](#TOC-instalacion)
2. [Encapsulamiento](#TOC-encap)
3. [Selectores](#TOC-selectores)
4. [Atributos](#TOC-atributos)
5. [Clases](#TOC-clases)
6. [Manipular DOM](#TOC-dom)
7. [Eventos](#TOC-eventos)


## <a name="TOC-instalacion"></a>Instalación
Para usar Jquery dirigirse a [JQuery](https://jquery.com/download/) , descargar el archivo js e importarlo en el html.
Recordar colocar lo siguiente para escribir código Jquery:
```javascript
$(document).ready(function() {

    //DOM manipulation code

});
```

## <a name="TOC-encap"></a>Encapsulamiento
```javascript
(function(){
  //Escribir código aquí
})();
```

## <a name="TOC-selectores"></a>Selectores
```javascript
//Selector de clase:
$(".nombreClase")

//Selector de html:
$("ul")

//Selector de id:
$("#nombreID")
```
## <a name="TOC-atributos"></a>Atributos
```javascript
//obtener el valor de un atributo y guardarlo en variable
var atributo = $("#imagen-large").attr("alt");

//reemplazar el valor de un atributo
var src = "una url";
$("#imagen-large").attr("src",src);
```

## <a name="TOC-clases"></a>Clases
```javascript
//añadir una clase a un elemento
$("#id").addClass("btn-primary")

//eliminar una clase a un elemento
$("#id").removeClass("btn-primary")
```
## <a name="TOC-dom"></a>Manipular DOM
```javascript
//Eliminar todos los elementos hijos dentro del padre
$('#body-table').empty();

//Concatenar un string para hacer una linea de table y añadirla al final
var linea = '';
linea += "<tr>";
linea += "<td>"+myNumber+"</td>;"
linea += "<td>x</td>;"
linea += "<td>"+contador+"</td>";
linea += "<td>=</td>";
linea += "<td>"+resultado+"</td>";
$('#body-table').append(linea);

//Cambiar el texto de un elemento html
$('#small-name').text("Texto");
$('#small-name').html("<p>Texto</p>");
```
## <a name="TOC-eventos"></a>Eventos
```javascript
//evento click  
$('#btn-add').on("click",function(){

});

//al pasar el mouse sobre algo se activa
$(".cursor-mano").on("mouseover",function(){

});

//al retirar el mouse del elemento
$(".cursor-mano").on("mouseleave",function(){

});

//detener comportamiento de href
$('#enlace').on("click",function(e){
    e.preventDefault();
    var link = $(this).attr("href") //el this hace referencia al mismo elemento que se selecciono.
    //hacer algun comportamiento aquí...
    //redirigir
    window.location = link
});
```
