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