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