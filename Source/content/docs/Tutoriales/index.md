---
title: 'Tutoriales'
date: 2020-06-17T19:30:08+10:00
draft: false
weight: 3
summary: Tutorial de configuración básica del menú y otros elementos del tema.
---

# Configuracion

<!-- Contenido del Post -->

## Highlighting de Código

Este tema utiliza el resaltado de código incorporado que se incluye con Hugo. https://gohugo.io/content-management/syntax-highlighting/

Puede insertar fragmentos de código en cualquier Markdown utilizando la sintaxis de highlighting, es decir:

````
```
insertar código acá
```
````

Puede especificar el lenguaje de programación agregando una declaración después de los backticks

````
```html
insertar código acá
```
````

### Opciones de resaltado de código 

Las opciones de resaltado de código se configuran en `config.toml`

```toml
pygmentsCodeFences = true
pygmentsCodefencesGuessSyntax = true
pygmentsUseClasses = true
```

## Menú principal

Configure el menú principal editando el `config.toml`

```toml
[[menu.main]]
    name = "Inicio"
    url = "/"
    weight = 1

[[menu.main]]
    name = "Documentación"
    url = "/docs/"
    weight = 2
```

# Instalar Tema

<!-- Contenido del Post -->

## Crear un nuevo sitio Hugo

```
hugo new site misitio
```

Esto creará un nuevo sitio de Hugo en la carpeta `misitio`.

## Instalar sitio Hugo

Copie o clone con git el sitio en la carpeta carpeta `misitio`.

## Ejecutar Hugo

Para el desarrollo de manera local, ejecute el servidor incorporado con Hugo utilizando la terminal de comandos.

```
hugo server
```
Ahora ingresa a [`localhost:1313`](http://localhost:1313) en la barra de URL de su navegador.

Después de editar el contenido y generar el sitio web, obtenga el compilado de archivos web a través del siguiente comando en la terminal. Este comando generará una carpeta `public` al interior de la carpeta del sitio web.

```
hugo
```

# Ejemplo Shortcodes

<!-- Ejemplo Shortcodes -->

# Contenido Shortcodes

- [Iframe de Fusion 360](#agregar-iframe-de-fusion-360)
- [Agregar Video Local MP4](#agregar-video-local-mp4)
- [Galería Fotos Lightbox](#agregar-galería-fotos-lightbox)
- [Botón de Descarga](#agregar-botón-de-descarga)

<!-- Agregar Iframe de Fusion 360 -->
---

### Agregar Iframe de Fusion 360

{{< iframe-fusion >}}

##### Código `Iframe de Fusion 360` Markdown 

```
{{</* iframe-fusion */>}}
```

##### Código `Iframe de Fusion 360` HTML Shortcode 

```
<div>
    <iframe 
    src="https://myhub.autodesk360.com/ue2ce4e3a/shares/public/SH56a43QTfd62c1cd968edbffd1ceafd2764?mode=embed" 
    width="100%" 
    height="450" 
    allowfullscreen="true" 
    webkitallowfullscreen="true" 
    mozallowfullscreen="true"  
    frameborder="0">
    </iframe>    
</div>
```

[[Volver Arriba]](#contenido-shortcodes)

<!-- Agregar Video Local MP4 -->
---

### Agregar Video Local MP4

{{< video-local src="video.mp4" >}}

##### Código `Video Local MP4` Markdown 

```
{{</* video-local src="video.mp4" */>}}
```

##### Código `Video Local MP4` HTML Shortcode 

```
<div>
    <video 
    width="100%" 
    height="450" 
    autoplay muted loop controls preload>
    <source src="/{{ index .Params "src" }}"  type="video/mp4">
    </video>
</div>
```

[[Volver Arriba]](#contenido-shortcodes)
 
<!-- Agregar Galería Fotos Lightbox -->
---

### Agregar Galería Fotos Lightbox

{{< gallery dir="/img/galeria/" />}} {{< load-photoswipe >}}

##### Código `Galería Fotos Lightbox` Markdown 

```
{{</* gallery dir="/img/galeria/" />}} {{< load-photoswipe */>}}
```

[[Volver Arriba]](#contenido-shortcodes)

<!-- Agregar Botón de Descarga -->
---

### Agregar Botón de Descarga

{{< boton-descargar src="documento.pdf" >}}

##### Código `Botón de Descarga` Markdown 

```
{{</* boton-descargar src="documento.pdf" */>}}
```

##### Código `Botón de Descarga` HTML Shortcode 

```
<a class="face-button" href="/descargas/{{ index .Params "src" }}" download>
    <div class="face-primary">
        <span class="icon fa fa-cloud"></span>
        Descargar
    </div>
    <div class="face-secondary">
        <span class="icon fa fa-hdd-o"></span>
    </div>
</a>
```

[[Volver Arriba]](#contenido-shortcodes)
 
# Ejemplos Markdowns

<!-- Ejemplos de códigos Markdown -->

# <a name="top"></a>Ejemplos de códigos Markdown

- [Headings](#headings)
- [Párrafos](#párrafos)
- [Citado](#citado)
- [Listas](#listas)
- [Línea Horizontal](#línea-horizontal)
- [Tabla](#tabla)
- [Código](#código)
- [Elementos e Imágenes](#elementos-e-imágenes-en-línea)

---

# Headings

# Heading one

Sint sit cillum pariatur eiusmod nulla pariatur ipsum. Sit laborum anim qui mollit tempor pariatur nisi minim dolor. Aliquip et adipisicing sit sit fugiat commodo id sunt. Nostrud enim ad commodo incididunt cupidatat in ullamco ullamco Lorem cupidatat velit enim et Lorem.

## Heading two

Aute officia nulla deserunt do deserunt cillum velit magna. Officia veniam culpa anim minim dolore labore pariatur voluptate id ad est duis quis velit dolor pariatur enim. Incididunt enim excepteur do veniam consequat culpa do voluptate dolor fugiat ad adipisicing sit.

### Heading three

Voluptate cupidatat cillum elit quis ipsum eu voluptate fugiat consectetur enim. Quis ut voluptate culpa ex anim aute consectetur dolore proident voluptate exercitation eiusmod. Esse in do anim magna minim culpa sint. Adipisicing ipsum consectetur proident ullamco magna sit amet aliqua aute fugiat laborum exercitation duis et.

#### Heading four

Commodo fugiat aliqua minim quis pariatur mollit id tempor. Non occaecat minim esse enim aliqua adipisicing nostrud duis consequat eu adipisicing qui. Minim aliquip sit excepteur ipsum consequat laborum pariatur excepteur.

##### Heading five

Veniam enim esse amet veniam deserunt laboris amet enim consequat. Minim nostrud deserunt cillum consectetur commodo eu enim nostrud ullamco occaecat excepteur. Aliquip et ut est commodo enim dolor amet sint excepteur. Amet ad laboris laborum deserunt sint sunt aliqua commodo ex duis deserunt enim est ex labore ut.

###### Heading six

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

[[Volver Arriba]](#top)

# Párrafos

Incididunt ex adipisicing ea ullamco consectetur in voluptate proident fugiat tempor deserunt reprehenderit ullamco id dolore laborum. Do laboris laboris minim incididunt qui consectetur exercitation adipisicing dolore et magna consequat magna anim sunt. Officia fugiat Lorem sunt pariatur incididunt Lorem reprehenderit proident irure. Dolore ipsum aliqua mollit ad officia fugiat sit eu aliquip cupidatat ipsum duis laborum laborum fugiat esse. Voluptate anim ex dolore deserunt ea ex eiusmod irure. Occaecat excepteur aliqua exercitation aliquip dolor esse eu eu.

Officia dolore laborum aute incididunt commodo nisi velit est est elit et dolore elit exercitation. Enim aliquip magna id ipsum aliquip consectetur ad nulla quis. Incididunt pariatur dolor consectetur cillum enim velit cupidatat laborum quis ex.

Officia irure in non voluptate adipisicing sit amet tempor duis dolore deserunt enim ut. Reprehenderit incididunt in ad anim et deserunt deserunt Lorem laborum quis. Enim aute anim labore proident laboris voluptate elit excepteur in. Ex labore nulla velit officia ullamco Lorem Lorem id do. Dolore ullamco ipsum magna dolor pariatur voluptate ipsum id occaecat ipsum. Dolore tempor quis duis commodo quis quis enim.

[[Volver Arriba]](#top)

# Citado

Ad nisi laborum aute cupidatat magna deserunt eu id laboris id. Aliquip nulla cupidatat sint ex Lorem mollit laborum dolor amet est ut esse aute. Nostrud ex consequat id incididunt proident ipsum minim duis aliqua ut ex et ad quis. Laborum sint esse cillum anim nulla cillum consectetur aliqua sit. Nisi excepteur cillum labore amet excepteur commodo enim occaecat consequat ipsum proident exercitation duis id in.

> Ipsum et cupidatat mollit exercitation enim duis sunt irure aliqua reprehenderit mollit. Pariatur Lorem pariatur laboris do culpa do elit irure. Eiusmod amet nulla voluptate velit culpa et aliqua ad reprehenderit sit ut.

Labore ea magna Lorem consequat aliquip consectetur cillum duis dolore. Et veniam dolor qui incididunt minim amet laboris sit. Dolore ad esse commodo et dolore amet est velit ut nisi ea. Excepteur ea nulla commodo dolore anim dolore adipisicing eiusmod labore id enim esse quis mollit deserunt est. Minim ea culpa voluptate nostrud commodo proident in duis aliquip minim.

> Qui est sit et reprehenderit aute est esse enim aliqua id aliquip ea anim. Pariatur sint reprehenderit mollit velit voluptate enim consectetur sint enim. Quis exercitation proident elit non id qui culpa dolore esse aliquip consequat.

Ipsum excepteur cupidatat sunt minim ad eiusmod tempor sit.

> Deserunt excepteur adipisicing culpa pariatur cillum laboris ullamco nisi fugiat cillum officia. In cupidatat nulla aliquip tempor ad Lorem Lorem quis voluptate officia consectetur pariatur ex in est duis. Mollit id esse est elit exercitation voluptate nostrud nisi laborum magna dolore dolore tempor in est consectetur.

Adipisicing voluptate ipsum culpa voluptate id aute laboris labore esse fugiat veniam ullamco occaecat do ut. Tempor et esse reprehenderit veniam proident ipsum irure sit ullamco et labore ea excepteur nulla labore ut. Ex aute minim quis tempor in eu id id irure ea nostrud dolor esse.

[[Volver Arriba]](#top)

# Listas

### Lista Enumerada

1. Longan
2. Lychee
3. Excepteur ad cupidatat do elit laborum amet cillum reprehenderit consequat quis.
   Deserunt officia esse aliquip consectetur duis ut labore laborum commodo aliquip aliquip velit pariatur dolore.
4. Marionberry
5. Melon
   - Cantaloupe
   - Honeydew
   - Watermelon
6. Miracle fruit
7. Mulberry

### Lista con Guiones

- Olive
- Orange
  - Blood orange
  - Clementine
- Papaya
- Ut aute ipsum occaecat nisi culpa Lorem id occaecat cupidatat id id magna laboris ad duis. Fugiat cillum dolore veniam nostrud proident sint consectetur eiusmod irure adipisicing.
- Passionfruit

[[Volver Arriba]](#top)

# Línea Horizontal

In dolore velit aliquip labore mollit minim tempor veniam eu veniam ad in sint aliquip mollit mollit. Ex occaecat non deserunt elit laborum sunt tempor sint consequat culpa culpa qui sit. Irure ad commodo eu voluptate mollit cillum cupidatat veniam proident amet minim reprehenderit.

---

In laboris eiusmod reprehenderit aliquip sit proident occaecat. Non sit labore anim elit veniam Lorem minim commodo eiusmod irure do minim nisi. Dolor amet cillum excepteur consequat sint non sint.

[[Volver Arriba]](#top)

# Tabla

Duis sunt ut pariatur reprehenderit mollit mollit magna dolore in pariatur nulla commodo sit dolor ad fugiat. Laboris amet ea occaecat duis eu enim exercitation deserunt ea laborum occaecat reprehenderit. Et incididunt dolor commodo consequat mollit nisi proident non pariatur in et incididunt id. Eu ut et Lorem ea ex magna minim ipsum ipsum do.

| Tabla Heading 1 | Tabla Heading 2 | Center align | Right align | Tabla Heading 5 |
| :-------------- | :-------------- | :----------: | ----------: | :-------------- |
| Item 1          | Item 2          |    Item 3    |      Item 4 | Item 5          |
| Item 1          | Item 2          |    Item 3    |      Item 4 | Item 5          |
| Item 1          | Item 2          |    Item 3    |      Item 4 | Item 5          |
| Item 1          | Item 2          |    Item 3    |      Item 4 | Item 5          |
| Item 1          | Item 2          |    Item 3    |      Item 4 | Item 5          |

Minim id consequat adipisicing cupidatat laborum culpa veniam non consectetur et duis pariatur reprehenderit eu ex consectetur. Sunt nisi qui eiusmod ut cillum laborum Lorem officia aliquip laboris ullamco nostrud laboris non irure laboris. Cillum dolore labore Lorem deserunt mollit voluptate esse incididunt ex dolor.

[[Volver Arriba]](#top)

# Código

## Código en línea

Ad amet irure est magna id mollit Lorem in do duis enim. Excepteur velit nisi magna ea pariatur pariatur ullamco fugiat deserunt sint non sint. Duis duis est `Código in text` velit velit aute culpa ex quis pariatur pariatur laborum aute pariatur duis tempor sunt ad. Irure magna voluptate dolore consectetur consectetur irure esse. Anim magna `<strong>in culpa qui officia</strong>` dolor eiusmod esse amet aute cupidatat aliqua do id voluptate cupidatat reprehenderit amet labore deserunt.

## Highlighted

Et fugiat ad nisi amet magna labore do cillum fugiat occaecat cillum Lorem proident. In sint dolor ullamco ad do adipisicing amet id excepteur Lorem aliquip sit irure veniam laborum duis cillum. Aliqua occaecat minim cillum deserunt magna sunt laboris do do irure ea nostrud consequat ut voluptate ex.

```
Código o detalle en línea
```

Ex amet id ex aliquip id do laborum excepteur exercitation elit sint commodo occaecat nostrud est. Nostrud pariatur esse veniam laborum non sint magna sit laboris minim in id. Aliqua pariatur pariatur excepteur adipisicing irure culpa consequat commodo et ex id ad.

[[Volver Arriba]](#top)

# Elementos e Imágenes en línea

Sint ea anim ipsum ad commodo cupidatat do **exercitation** incididunt et minim ad labore sunt. Minim deserunt labore laboris velit nulla incididunt ipsum nulla. Ullamco ad laborum ea qui et anim in laboris exercitation tempor sit officia laborum reprehenderit culpa velit quis. **Consequat commodo** reprehenderit duis [irure](#!) esse esse exercitation minim enim Lorem dolore duis irure. Nisi Lorem reprehenderit ea amet excepteur dolor excepteur magna labore proident voluptate ipsum. Reprehenderit ex esse deserunt aliqua ea officia mollit Lorem nulla magna enim. Et ad ipsum labore enim ipsum **cupidatat consequat**. Commodo non ea cupidatat magna deserunt dolore ipsum velit nulla elit veniam nulla eiusmod proident officia.

![Imagen Simple](/img/imagen.jpg)

_Proident sit veniam in est proident officia adipisicing_ ea tempor cillum non cillum velit deserunt. Voluptate laborum incididunt sit consectetur Lorem irure incididunt voluptate nostrud. Commodo ut eiusmod tempor cupidatat esse enim minim ex anim consequat. Mollit sint culpa qui laboris quis consectetur ad sint esse. Amet anim anim minim ullamco et duis non irure. Sit tempor adipisicing ea laboris `culpa ex duis sint` anim aute reprehenderit id eu ea. Aute [excepteur proident](#!) Lorem minim adipisicing nostrud mollit ad ut voluptate do nulla esse occaecat aliqua sint anim.

Incididunt in culpa cupidatat mollit cillum qui proident sit. In cillum aliquip incididunt voluptate magna amet cupidatat cillum pariatur sint aliqua est _enim **anim** voluptate_. Magna aliquip proident incididunt id duis pariatur eiusmod incididunt commodo culpa dolore sit. Culpa do nostrud elit ad exercitation anim pariatur non minim nisi **adipisicing sunt _officia_**. Do deserunt magna mollit Lorem commodo ipsum do cupidatat mollit enim ut elit veniam ea voluptate.

[![Imagen Box](https://img.youtube.com/vi/qEuD6v1Y9fg/0.jpg)](https://www.youtube.com/watch?v=9sttGOpz7VY)

Reprehenderit non eu quis in ad elit esse qui aute id [incididunt](#!) dolore cillum. Esse laboris consequat dolor anim exercitation tempor aliqua deserunt velit magna laboris. Culpa culpa minim duis amet mollit do quis amet commodo nulla irure.