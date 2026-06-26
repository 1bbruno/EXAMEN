# EXAMEN
# Pensamiento-computacional-EXAMEN

## 1. Información del proyecto

**Nombre del proyecto:**
Flying over the city

**Autor:**
Bruno Jara
---

## 2. Descripción objetiva

Este proyecto consiste en un sistema visual dinámico e interactivo creado en p5.js. La propuesta toma como base la corriente visual de los 2000 **Frutiger Metro**, reinterpretando sus elementos gráficos a través de un sistema computacional.

En pantalla se genera una composición visual de 800 x 700 píxeles formada por círculos concéntricos, una silueta de ciudad y símbolos gráficos decorativos. El sistema toma elementos característicos de Frutiger Metro como la repetición de formas vectoriales, colores saturados, elementos urbanos y gráficos inspirados en interfaces digitales de los años 2000.

Los elementos visuales principales son:

* Círculos concéntricos que aumentan y se repiten dentro del espacio en diagonal.
* Una ciudad creada a partir de figuras geométricas simples.
* Símbolos decorativos que son un avión y un ovni.
* Dos paletas de color: una paleta de colores azulados y una paleta de alto contraste rosado/negro/blanco.

El sistema utiliza como input principal la posición vertical del mouse. También utiliza las teclas **A**, **S**, **D** y **W** para los movimientos, además del click del mouse para generar nuevas variaciones visuales.

Como output, el sistema genera una composición gráfica que cambia en tiempo real modificando cantidad de elementos, colores, símbolos y tamaños.

---

# 3. Descripción conceptual

La idea central del proyecto es reinterpretar la lógica visual de **Frutiger Metro*. En lugar de copiar una imagen específica de la corriente, el proyecto traduce sus principios principales: acumulación visual, repetición, capas gráficas y mezcla entre elementos tecnológicos y decorativos.

El proyecto dialoga con el diseño de interfaces y la gráfica digital de mediados de los 2000, donde era común encontrar composiciones con elementos vectoriales, círculos, brillos, naturaleza artificial y formas superpuestas.

### Referentes visuales, teóricos o históricos

**Frutiger Metro:**
Principal referente del proyecto. Se toma su uso de formas vectoriales, círculos concéntricos, colores saturados, elementos urbanos y composición maximalista.

**Diseño de interfaces de los 2000:**
Se utiliza como referencia la estética de fondos digitales, publicidad e interfaces que mezclaban tecnología con elementos decorativos y orgánicos.

**Diseño vectorial Y2K:**
Se toma la idea de construir imágenes mediante formas simples, repetidas y fácilmente modificables mediante reglas.

### Principio de diseño explorado

El principio de diseño explorado es la **repetición con variación**.

Los círculos funcionan como un sistema donde una misma forma se repite, pero cambia dependiendo de reglas definidas por el código como:

* cantidad
* posición
* tamaño
* color

También se explora la interacción entre usuario y sistema, donde una composición visual cambia constantemente dependiendo de las decisiones del usuario.

---

## 4. Input / Output y sistema

### Inputs
El proyecto utiliza distintas entradas del usuario para controlar la experiencia interactiva:

* **Click del mouse:** 
* 1.Inicia la experiencia
* 2.Cambia el símbolo entre 🛩️ y 🛸.
* 3.Reproduce un efecto de sonido.
* 4.Aumenta el contador de cambios.
* 5.Modifica aleatoriamente el tamaño del símbolo.
* **Teclas del teclado:**
* A: mueve el símbolo hacia la izquierda.
* D: mueve el símbolo hacia la derecha.
* W: mueve el símbolo hacia arriba.
* S: mueve el símbolo hacia abajo.
* 1: alterna entre dos paletas de colores del fondo.
* Posición vertical del mouse
Controla la cantidad de círculos que aparecen en la composición mediante la función map().
---

### Procesos

El programa procesa las entradas del usuario para modificar el estado de la experiencia.

* Comienza mostrando una pantalla de inicio hasta que el usuario hace click.
* Dibuja un fondo cuyo color cambia según la paleta seleccionada.
* Genera una composición de círculos cuya cantidad depende de la posición del mouse.
* Dibuja una ciudad utilizando rectángulos y ventanas repetidas mediante bucles.
* Muestra un emoji (🛩️ o 🛸) que cambia con cada click y cuyo tamaño es aleatorio.
* Reproduce sonidos al iniciar, durante la interacción y al llegar a la pantalla final.
* Cuenta la cantidad de movimientos realizados con las teclas WASD.
* Cuenta la cantidad de cambios del símbolo realizados mediante clicks.
* Detecta cuándo el símbolo alcanza el borde derecho de la pantalla para finalizar la experiencia.

---

### Outputs

La aplicación responde visual y sonoramente a las acciones del usuario.

* Pantalla de inicio con instrucciones.
* Fondo dinámico con dos paletas de colores.
* Círculos que cambian de cantidad según el movimiento del mouse.
* Ciudad construida con figuras geométricas.
* Símbolo (🛩️ / 🛸) cuyo tamaño y tipo cambian durante la interacción.
* Reproducción de sonidos de inicio, interacción y final.
* Pantalla final que muestra:
* Mensaje "LOGRADO".
* Cantidad de movimientos realizados.
* Cantidad de cambios del símbolo.

---

### Reglas del sistema

* La experiencia comienza únicamente después del primer click.
* Cada click alterna el símbolo entre 🛩️ y 🛸.
* Cada click aumenta el contador de cambios.
* Las teclas A, S, D y W desplazan el símbolo y aumentan el contador de movimientos.
* La tecla 1 alterna entre dos paletas de colores.
* Cuando el símbolo alcanza el borde derecho del lienzo, se activa la pantalla final.
* Una vez en la pantalla final:
- deja de ser posible mover el símbolo;
- dejan de contarse movimientos y cambios;
- se reproduce el sonido final una única vez;
- se muestran las estadísticas de la partida.

---
# Explicación de la interacción

## ¿Qué datos entran al sistema?

El sistema recibe información a partir de las acciones del usuario:

* Click del mouse.
* Pulsación de las teclas **A**, **S**, **D**, **W** y **1**.
* Posición vertical del mouse (`mouseY`).

---

## ¿Cómo se procesan?

Cada entrada modifica variables internas que controlan el estado de la experiencia.

* El primer click inicia la partida.
* Cada click alterna el símbolo entre 🛩️ y 🛸.
* Cada click genera un tamaño aleatorio para el símbolo.
* Las teclas **A**, **S**, **D** y **W** actualizan la posición del símbolo y aumentan el contador de movimientos.
* La tecla **1** cambia la paleta de colores.
* La posición vertical del mouse determina la cantidad de círculos que se dibujan.
* Cuando el símbolo alcanza el borde derecho de la pantalla, el sistema cambia al estado de pantalla final.

---

## ¿Cómo se transforman?

Las entradas del usuario se convierten en cambios visuales y sonoros.

* El símbolo cambia entre avión y ovni.
* El tamaño del símbolo cambia de forma aleatoria.
* El fondo alterna entre dos paletas de colores.
* La cantidad de círculos aumenta o disminuye según la posición del mouse.
* Se actualizan los contadores de movimientos y cambios.
* Se activa la pantalla final al completar el recorrido.

---

## ¿Qué respuestas producen?

El sistema responde mostrando y reproduciendo distintos elementos:

* Pantalla de inicio con instrucciones.
* Escenario interactivo compuesto por una ciudad y círculos.
* Movimiento y transformación del símbolo.
* Sonidos de inicio, interacción y final.
* Pantalla final con las estadísticas de la partida:

  * Cantidad de movimientos.
  * Cantidad de cambios del símbolo.

---

# Recursos multimedia utilizados

## Recursos de audio

### Sonido de inicio

* **Tipo de recurso:** Archivo de audio inicial (.wav).
* **Función:** Se reproduce cuando el usuario inicia la experiencia mediante el primer click.

### Sonido de interacción

* **Tipo de recurso:** Archivo de audio secundario (.wav).
* **Función:** Se reproduce cada vez que el usuario hace click para cambiar el símbolo.

### Sonido de pantalla final

* **Tipo de recurso:** Archivo de audio (.mp3).
* **Función:** Se reproduce una única vez al llegar a la pantalla final, marcando el cierre de la experiencia.

---

## Recursos gráficos

### Símbolos (🛩️ y 🛸)

* **Tipo de recurso:** Emojis Unicode.
* **Función:** Representan el elemento principal de la interacción y alternan con cada click del usuario.

### Ciudad y círculos

* **Tipo de recurso:** Gráficos generados mediante código en p5.js.
* **Función:** Construyen el escenario visual y responden a las acciones del usuario.

### Textos

* **Tipo de recurso:** Texto generado mediante p5.js.
* **Función:** Presentan las instrucciones al usuario y muestran las estadísticas en la pantalla final.

## 5. Diagrama de flujo

![Diagrama de flujo](./imagenes/diagrama-flujo.png)

---

## 6. Imágenes

### Referentes visuales

![Referente Frutiger Metro](https://github.com/1bbruno/EXAMEN/blob/6a32e7f6cac3fa79d475fcbe6c14a1ea1f6c7498/imagenesconceptuales/3ae8f2d3eab64011eeecf50bcbb8b42e.jpg)

![Referente Frutiger Metro](https://github.com/1bbruno/EXAMEN/blob/d4b45c9f8fabf05cdc7b71420a35733d6c30a94b/imagenesconceptuales/431bf15cfa6bbab3f2186c1a518c2da1.jpg)

![Referente Frutiger Metro](https://github.com/1bbruno/EXAMEN/blob/c2a8f0ee8a5eb8d2feaba6a62888d25f9a7f3141/imagenesconceptuales/d53fa06872a18e4a35fdf23a780eae0d.jpg)

### Proceso

![Proceso](./imagenes/proceso.gif)

---

## 7. Link al sketch en p5.js

[Link al sketch en p5.js](https://editor.p5js.org/1bruno/sketches/6Cv2f6d-C)

---

## 8. Bitácora breve del proceso

Primero definímos trabajar con la corriente Frutiger Metro debido a su relación con sistemas digitales, interfaces y gráficos vectoriales de los años 2000.

El primer paso fue construir los círculos concéntricos, ya que son uno de los elementos visuales más reconocibles de esta estética. Luego se utilizó un bucle para transformar un solo círculo en un sistema repetitivo.

Después se incorporó el movimiento del mouse utilizando `map()`, permitiendo que la cantidad de círculos cambie en tiempo real según la interacción del usuario.

Más adelante se agregó una silueta de ciudad creada con figuras geométricas simples, reforzando la relación con la estética urbana y digital del referente.

Luego se incorporaron símbolos gráficos como estrellas y flores mediante texto, haciendo referencia a los elementos decorativos utilizados en esta corriente visual.

Finalmente se agregaron cambios de paleta mediante teclado para generar diferentes versiones de la composición.

El resultado final es un sistema visual interactivo que transforma una estética gráfica estática en una composición generativa controlada por reglas, repetición e interacción.

## 9. Codigo escrito

//variables 
let paleta = 0;
let simbolo = "🛩️";
let sonido = false;
let sonidoinicio = false;
let sonidoetapafinal = false; 
let partidaIniciada = false;  //EXPERIENCIA
let etapaFinal = false;     //FINAL
let contadormovimientos = 0;
let clicks = 0;

//variables de posición y tamaño del símbolo que aparece
let simboloX = 0;
let simboloY = 250;
let simboloTam = 0;
let mostrarSimbolo = true;





//tamaño del setup
function setup() {
  createCanvas(800, 700);
}





//funciones que construyen el visual
function draw() {

    //si la partida esta iniciada, muesta la funcion dibujarInicio
  if (!partidaIniciada == true) {
    dibujarInicio ();
  } 
    // cuando inicia la partida, el contrario que se activa es la etapaFinal
  else if (etapaFinal) {

    //el sonido que se activa en la pantalla final
    if (!sonidoetapafinal) {
      sonidofinal.play ();
      sonidoetapafinal = true;
    }
    
    dibujarFinal ();
  } 
    //demas funciones esteticas
  else {
  dibujarFondo();
  dibujarCirculos();
  dibujarCiudad();
  dibujarEmoji();
}
 }





// MENU DE LA EXPERIENCIA
function dibujarInicio() {
  //color de inicio y la velocidad de carga
  background (250, 20 , 250, 5);

  //edificios superiores
  noStroke ();
  fill (100,40,160)
  rect(80, 0, 90, 120);
  rect(230, 0, 80, 170);
  rect(390, 0, 100, 290);
  rect(560, 0, 110, 140);

  //edificios inferiores
  fill (160,40,100)
  rect(390,  600, 90, 120);
  rect(230, 550, 80, 200);
  rect(80, 450, 100, 290);
  rect(560, 600, 110, 140);

  
  //se muestra en el inicio de la partida
  if (!partidaIniciada == true) {
  textAlign (CENTER, CENTER);
    
  textSize (40);
    stroke (0);
    strokeWeight (5);
  fill (130, 90, 200);
  text ("CLICK PARA INICIAR...", width/2, height/2);

    textSize (80)
    stroke (255,255,0)
    strokeWeight (7)
    fill (0, 0, 250)
    text("Flying over the city", 400, 100)
}
}






//cargar elementos
function preload (){
  sonidoinicio = loadSound("sonidoinicio.wav");
  sonido = loadSound("efecto.wav");
  sonidofinal = loadSound("sonidofinal.mp3");
  
}







function mousePressed() {

   //con el mouse presionado cambia entre avión y ovni
  if (simbolo == "🛩️") {
    simbolo = "🛸"
  } else {
  simbolo = "🛩️";
}
 

  //si la partida esta iniciada este sonido se activa 
   if (!partidaIniciada) {
    sonidoinicio.play();
  }

  //en la etapa final el return anula los clicks y los sonidos para que no los siga contando
  if(etapaFinal) {
    return;
  }

  //click que se cuentan, debajo para que en la pantalla final no los cuente
   clicks++;

  //sonido, debajo del return para que no suene al final. los click encienden el sonido
  sonido.play();
  
  //si todavía no comienza, iniciar la partida haciendo click
  if (!partidaIniciada) {
    partidaIniciada = true;   
  }

  //tamaño aleatorio del simbolo con cada click
  simboloTam = random(70, 260);
  mostrarSimbolo = true;
}





function dibujarFondo() {

    //cambia los colores dependiendo de la paleta seleccionada
  if (paleta == 0) {
    background(0, 0, 255);
  } else {
    background(245, 30, 130);
  }
  //texto de instrucciones
  fill(255);
  textSize(10);
  textAlign(LEFT, TOP);
  noStroke();
  
 //texto de instrucciones 
  text('"A" izquierda', 20, 20);
  text('"S" abajo', 20, 40);
  text('"D" derecha', 20, 60);
  text('"W" arriba', 20, 80);
  text('"1" para alternar fondo', 90, 20)
  text("Click para alternar nave", 90, 40)
  text("Muevete hasta la derecha", 90, 60)
}




function dibujarCirculos() {
  
   //la posición vertical del mouse controla la cantidad de círculos
  let cantidad = map(mouseY, 0, height, 3, 14);
  cantidad = int(cantidad);

  noFill();

  // colores de circulos dependiendo de paleta
  if (paleta == 0) {
    stroke(255, 0, 130);
  } else {
    stroke(255);
  }

   //bucle que genera los círculos repetidos 
  for (let i = 0; i < cantidad; i++) {
    
    //cada círculo avanza hacia el lado y baja creando una diagonal
 let x = 80 + i * 100;
 let y = 150 + i * 15;
    
    //el tamaño aumenta gradualmente
    let tam = 80 + i * 20;

    //círculo exterior
    strokeWeight(8);
    circle(x, y, tam);

    //círculo interior
    strokeWeight(4);
    circle(x, y, tam * 0.55);
  }
}





function dibujarCiudad() {
  noStroke();

  //la ciudad cambia de color dependiendo de la paleta
  if (paleta == 0) {
    fill(0, 0, 90);
  } else {
    fill(0, 0, 0);
  }

  //edificios creados con rectángulos y el suelo
  rect(0, 600, width, 200);
  rect(80, 500, 90, 120);
  rect(230, 450, 80, 170);
  rect(390, 330, 100, 290);
  rect(560, 480, 110, 140);

  // color de suelo y edificios)
  fill(255, 240, 80, 170);

  //bucle para repetir ventanas
for (let x = 95; x < 670; x += 25) {
  for (let y = 360; y < 590; y += 25) {
    rect(x, y, 8, 5);
  }
}
}





function dibujarEmoji() {

  //solo aparece cuando el usuario hace click
  if (mostrarSimbolo == true) {
    textAlign(CENTER, CENTER);
    textSize(simboloTam);
//colores del símbolo según la paleta actual 
    if (paleta == 0){
      fill(255, 0, 170); 
      stroke(255, 0, 170);
    } else {
      fill(255); 
      stroke(0); 
    } strokeWeight(4);
    text(simbolo, simboloX, simboloY);
  } 
}





function dibujarFinal () {

  
  background (0);

   textAlign (CENTER, CENTER);

  // texto que aparece en la pantalla final
  fill (255, 255, 0);
  stroke(0, 0, 100);
  strokeWeight (10);
  textSize (100);
  text ("LOGRADO", 400, 200)

  fill(255, 0, 150)
  stroke (0, 0, 255);
  strokeWeight (5);
  textSize (30);
  text ("puntuación", 400, 300)

  fill (255, 0, 150);
  stroke (0, 0, 255);
  strokeWeight (5);
  textSize (50);
  
  //cantidad de los movimientos o cambios del simbolo a partir de las variables
  text ("Cantidad de Movimientos: " + contadormovimientos, 400, 400);
  text ("Cantidad de Cambios: " + clicks, 400, 500);
}







function keyPressed() {
  //si llego a la etapa final, con return deja de contar los movimientos
if (etapaFinal) {
    return;
  }

  //mover a la izquierda
  if (key == "a" || key == "A") {
  simboloX -= 20;
    contadormovimientos++;
}

  //mover hacia la derecha
if (key == "d" || key == "D") {
  simboloX += 20;
  contadormovimientos++;
}
  
  // mover hacia arriba
if (key == "w" || key == "W") {
  simboloY -= 20;
  contadormovimientos++;
}

  //mover hacia abajo
if (key == "s" || key == "S") {
  simboloY += 20;
  contadormovimientos++;
}
  
    //cuando el simbolo llega hasta width que es el borde derecho se activa la variable etapaFinal
  if (simboloX >= width - 20) {
    etapaFinal = true;
  }

  //tecla 1 cambia entre las dos paletas de color
  if (key == "1") {
    paleta = 1 - paleta;
  }
}
}
}
