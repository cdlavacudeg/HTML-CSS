# HTML -> Hyper Text Markup Lenguage

## Anatomia de un sitio web

- Header (Logo,Navegación)
- Main Content
- Sidebar
- Footer

## Tipos de imagenes

- Lossy:Con perdida, reducir al cantidad ded colores o datos inecesarios disminuyendo el tamaño del archivo.
- Lossless:Sin perdida no se pierde calidad, son pesadas.

### Formatos

- Gif (lossles):256 colores
- PNG 8(lossles): 256 colores, para usar transparente
- PNG 24 (lossles): colores ilimitados
- JPG/JPEG (lossy): Millones de colores ,se pierde calidad al comprimirlo
- SVG (lossles): Colores ilimitados, formato muy ligero, pantallaz de retina, no se pixelea.

### Optimización de imagenes

Promedio de tamaño 70Kb-100Kb.
- [Tiny PNG](https://tinypng.com/): mejorar tamaño  
- [Verefix](https://www.verexif.com/) :quita los meta datos  

### Etiqueta figure

Semanticamente es mas correcto que usar un div,imagenes con uno pequeña descripción
```
<figure>
    <img>
    <figcaption>Caption</figcaption>
</figure>
```

### Etiqueta de video

```
<video src="src#t=10,60" controls preload="auto">
    <source src="src1"/>
    <source src="src2"/>
    <source src="src3"/>
    <source src="src4"/>
</video>
```

### Formularios

#### Input
```
<form action="Link">
    <label for="label1">
        <span>Label 1:</span>
        <input type="text" id="label1" placeholder="ph" />
    </label>
    <label for="label2">
        <span>Label 2:</span>
        <input type="date" id="label2"/>
    </label>
    <label for="label3">
        <span>Label 1:</span>
        <input type="time" id="label3"/>
    </label>
</form>
```

```
<form>
        <label for="hora">
            <span>Hora</span>
            <input type="time" id="hora" name="hora"/>
        </label>
        <label for="dia">
            <span>Día</span>
            <input type="date" id="dia" name="dia"/>
        </label>
        <label for="semana">
            <span>Semana</span>
            <input type="week" id="semana" name="semana"/>
        </label>
        <label for="mes">
            <span>Mes</span>
            <input type="month" id="mes" name="mes"/>
        </label>
        <input type="submit"/>
</form>
```

```
<form action="">
        <label for="calendario">
            <input type="datetime-local" id="calendario" name="calendario">
        </label>
        <input type="submit"/>
</form>

```
[Link documentacion input](https://developer.mozilla.org/es/docs/Web/HTML/Element/input)

#### Autocomplete Required

```
<form action="">
    <label for="nombre">
        <span>¿Cual es tu nombre? </span>
        <input type="text" id="nombre" name="nombre" autocomplete="name" required />
    </label>
    
    <label for="correo">
        <span>¿Cual es tu correo? </span>
        <input type="email" id="correo" name="correo" autocomplete="email" required>
    </label>
    
    <label for="pais">
        <span>¿En que país vives?</span>
        <input type="text" id="pais" name="pais" autocomplete="country" required>
    </label>
    
    <label for="cp">
        <span>Código postal: </span>
        <input type="text" id="cp" name="cp" autocomplete="postal-code" required>
    </label>
    <input type="submit">
</form>

```

[Link documentacion autocomplete](https://developer.mozilla.org/es/docs/Web/HTML/Atributos/autocomplete)

### Select

```
<input list="cursos">
<datalist id="cursos">
    <option value="JS"></option>
    <option value="PHP"></option>
    <option value="REACT"></option>
    <option value="Python"></option>
</datalist>
```

### Botones

```
<input type="submit" value="Texto alternativo"> <!--formularios-->
<button type="submit">Texto alternativo</button>

```

## Links interesantes

Les comparto unas librerías que, les ayudarán para practicar.

[referencias CSS](https://cssreference.io/)  
[flexbox guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)  
[HTML](https://www.w3schools.com/html/default.asp)  

Un juego:
[FLEXBOX FROGGY](https://flexboxfroggy.com/#es)  

[Scroll bar styling](https://ed.team/blog/personaliza-el-scroll-de-tu-web-solo-con-css)  
[Compatibilidad con navegadores](https://caniuse.com/)
[Layouts](https://gridbyexample.com/patterns/)
[Design Guide](https://polaris.shopify.com/design/design)
[Neumorphismo](https://neumorphism.io/#e67070)
[CSS repositorio Platzi](https://github.com/platzi/CSS2020)
[Wireframes](https://app.moqups.com//#)
# CSS Grid y flexbox

## Flujo normal del documento

- `display: grid` -> `display: block(externo) grid(interno)`
- `display: inline-flex` -> interno comportamineto flex y externo inline.

## Formato de contexto de bloque (BFC)

Es un mini layout entre otra estructura o layout. Overflow:auto, position:absolute, position:fixed, display:inline-block/display:flow-root.

## Diferencias de CSS Grid y Flexbox

- Flexbox: distribuir el espacio entre los ítems y mejorar la alineación. Es unidireccional.´
- CSS Grid: alineación bidireccional.

### Flexbox

Container:
- display
- flex-direction
- flex-wrap
- flex-flow
- justify-content
- align-items
- align-content

Items:
- order
- flex-grow
- flex-shrink
- flex-basis
- flex
- align-self

### CSS grid

Container:
- display
- grid-template
- gap
- justify-items
- align-items
- justify-content
- align-content

Items:
- grid-column
- grid-row
- grid-area
- justify-self
- align-self

## Oneline -Layouts
[Link de los recursos](https://web.dev/one-line-layouts/)

- super-centered:
```
.parent {
  display: grid;
  place-items: center;
}
```
- The Deconstructed Pancake:
```
.parent {
  display: flex;
}

.child {
  flex: 0 1 150px;//flex: 1 1 150px;
}
```

- Sidebar Says:

```
.parent {
  display: grid;
  grid-template-columns: minmax(150px, 25%) 1fr;
}
```

- Pancake Stack:

```
.parent {
  display: grid;
  grid-template-rows: auto 1fr auto;
}
```

- Classic Holy Grail Layout:
```
.parent {
  display: grid;
  grid-template: auto 1fr auto / auto 1fr auto;
}
```

- 12-Span Grid:

```
.parent {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
}

.child-span-12 {
  grid-column: 1 / 13;
}

```
- RAM (Repeat, Auto, MinMax):

```
.parent {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
}
```

```
.parent {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
}
```

- Line Up:

```
.parent {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
```
## Figma
Algunos comandos básicos para ahorrar tiempo en Figma:

- Para crear un Frame solo oprime la tecla F.
- Para crear un rectángulo solo oprime la tecla R (si deseas un cuadrado perfecto oprime las teclas Shift + Option mientras arrastras el mouse, de esta forma crear un cuadrado en vez de un rectángulo)
- Para crear un circulo perfecto oprime la tecla O
- Para alinear un elemento en el centro del FRAME (de todo el frame, no del contenedor) oprime Option + H.
- Para alinear en el centro del Frame de forma vertical oprime Option + V
- Si desea cambiar el nombre de varios elementos al tiempo (Si te das cuenta en el panel izquierdo los elementos son nombrados como Rectangle 1, Rectangle 2, o Ellipse 1, Ellipse 2… Ellipse 9, etc y quizás tu los quieras llamar music button o player buttons) solo los seleccionas (puede ser dentro directamente en el Frame de diseño o seleccionas las capas en el panel izquierdo) y oprimes Command + R, de esta forma puedes renombrar muchos elementos al tiempo.