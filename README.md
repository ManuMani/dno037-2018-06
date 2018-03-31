# Clase 6 → Miércoles 11 de abril

### Canvas

**Canvas** es un elemento HTML. Literal y obviamente, se trata de un lienzo. Es usado para dibujar gráficos con scripts (normalmente JavaScript). En el código que sigue tengo un cuerpo (body) que, al cargarse (onload), ejecuta una función (pinta). Esta función pinta un cuadrilátero lleno, de tamaño 100 x 100 pixeles, ubicado a 25 pixeles del extremo izquierdo del lienzo y 25 pixeles de su extremo superior.

```
<body onload="pinta();">
<canvas id="este" width="150" height="150"></canvas>
<script>
function pinta() {
var canvas = document.getElementById('este');
if (canvas.getContext) {
var ctx = canvas.getContext('2d');
ctx.fillRect(25, 25, 100, 100);
  }
}
</script>
</body>
```

### p5.js 

[p5.js](https://p5js.org/es/get-started/) es una biblioteca de JavaScript creada para hacer la programación accesible a artistas, diseñadores, educadores y principiantes. Si ya conocen [Processing](https://processing.org/reference/), esta biblioteca se hará aún más accesible, a condición de recordar lo siguiente: Processing se basa en Java, mientras p5.js, que es una reinterpretación de Processing, se basa en JavaScript (Java y JavaScript se parecen tanto como una cama a un camarín; digo esto para que no se engañen con sus nombres, creyendo que el parecido podría ser como el de la cama al camarote).

Con p5.js podemos escribir scripts como "sketches". Éstos se ejecutarán dentro de un `<canvas></canvas>` que esta misma biblioteca de JavaScript se encarga de crear. Pronto notarán que, con p5.js, podremos dibujar gráficos con scripts más accesibles. Por ejemplo, algo como lo de arriba se escribiría de la siguiente manera:

```
<body>
<div id="este"></div>
<!--incluyo la biblioteca-->
<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.6.0/p5.min.js"></script>
<!--escribo el script/sketch-->
<script>
function setup() {
	var canvas = createCanvas(150, 150);
	canvas.parent('este');
}
function draw() {
	fill(0);
	rect(25,25,100,100);
}
</script>
</body>
```

Si necesitan referencias de p5.js, hay 2 posibilidades:

- Consultar [las referencias de la página de p5.js](https://p5js.org/es/reference/).

- Buscar a [Daniel Shiffman](http://shiffman.net/), el loquillo detrás de [The Coding Train](https://www.youtube.com/thecodingtrain/). Para este caso, recomendaría revisar las listas de producción de [p5.js tutorials - JavaScript, HTML, and CSS](https://www.youtube.com/user/shiffman/playlists?view=50&sort=dd&shelf_id=14)

- - - - - - 

[Clase anterior](https://github.com/profesorfaco/dno037-2018-05) | [Siguiente clase](https://github.com/profesorfaco/dno037-2018-07)
