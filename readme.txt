*********************utilizar componentCSS SuitCss************************
	no es mas que un estandar para nombrar clases en css "muy util"


**flex ó flex box***
antes llamado flexbox
es una nueva forma de hacer css y display de nuestros elementos

flex solo afecta al elemento y sus hijos directos

por defecto se pone uno al lado del otro

flex-direction column // para usarlo en forma de columna

**vh**
unidad de medidad que dice el alto del viewport 
min-height 100vh

**justify-content**
Medimos el justificado de la pagina
propiedades
	flex-stat
	flex-end alinear a la derecha
	flex-center centro
	space-between el primero izquierda ultimo derecha y el resto se distribulle en el centro(funciona verticalmente y horizontalmente)

	el mismo elemento debe de tener display:flex-box
flex:1 1; forma resumida de cuanto se puede estirar o achicar
		 toma el acho que hay en el esapcio libre es utili en los elmentos que quedan en medio despues del betwen


background-size cover//ajustar una background-image a toda la pantalla

text-transform uppercase//todo el texto en mayusculas


*****componentes*****
-Componente: Pequeña minima paret de tu aplicación que puedes abstraer y ser independiente
-Un componente tiene una parte de html, otra de css y otra de js

***npm***

manejador de paquetes de node 
permite instalar paquetes comos stylus jquery



instalar componente 
npm install nombre paquete
***stylus****

con node.js: nmp install stylus -g // para instalar stylus de forma global


compilar stylus
	stylus nombreArchivo.styl
compilar stylus y comprimir en una sola linea
	stylus nombreArchivo.styl -c
autocompilar stylus cada que ocurren cambios en el archivo .styl
	stylus nombreArchivo.styl -c -w

compilar en una ruta especifica
stylus -w -c -0 ruta_salida  archivo.styl

Usos
Concatenar clases a la clase padre
.Card
	
	&-description
		

	&-image
		width: 100%

lo anterior es igual a
.Card {
  
}
.Card-description {
 
}
.Card-image {
 
}

funciones en stylus
	test(color = red)//atributo con valor por defecto
		border 1px solid color
		box-sizing border-box
		

	.Layout
		display flex
		padding .5px
		margin .5em
		test()
		> section//heredando y gregando estilos a los hijos
			test(green)//enviando parametro para cambiar color
			margin .5em



****************jade**************jade-lang.com

Es una mejor forma de hacer html
Es un motor de template
Es un preprocesador de html


compilar jade
jade archivo.jade//compila y comprime en una sola linea

leer solo html
jade index.jade -P//"P" la p debe ser mayuscula


uso

con jade

doctype html
html(lang="es")
head
	meta(charset="utf-8")
	title Marvel Game Card
	link(rel="stylesheet", href="./public/css/app.css")
body
	section(class="Layout")
		section(class="Layout-angonist")
		section(class="Layout-main")
			div(class="Layaut-status") status
			div(class="Layout-battle") battle
			div(class="Layout-phases") phases
		section(class="Layout-player") player



sin jade

<!DOCTYPE html>
<html lang="es"></html>
<head>
  <meta charset="utf-8">
  <title>Marvel Game Card</title>
  <link rel="stylesheet" href="./public/css/app.css">
</head>
<body>
  <section class="Layout">
    <section class="Layout-angonist"></section>
    <section class="Layout-main">
      <div class="Layaut-status">status</div>
      <div class="Layout-battle">battle</div>
      <div class="Layout-phases">phases</div>
    </section>
    <section class="Layout-player">player</section>
  </section>
</body>

llamando un elemento jade y foreach

each card in [1,2,3,4,5]
	include ./card/template.jade



la variable card se puede recibir en el elemento car de la siguienete manera
	P= card

declarar variables
	- name = "Milton"//se pueden pasar a un archivo incluid de la misma forma p= name(el igual debe de estar pegado del elemento que lo va a contener)

*****nib****
Sirbe para poner mixin y poner compatibilidad en todos los navegadores con prefijos etc moz

instalar
npm install nib -g

usar:
 stylus -u nib -w -c -d ../public/css/ app.styl


 **********************HTTP********************
estados: 400,200,299,499

json:formato subconjunto javascript
















































