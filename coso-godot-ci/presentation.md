<!-- common CSS -->

<style>
.container{
    display: flex;
}
.col{
    flex: 1;
}
</style>

# Coso CI Godot

* Nepo nepo@mastodon
* Fernando taletronic@mastodon

(¡háblanos!)

---

# Casos de uso

  <!-- .slide: data-background="#ff0000" -->

* Día a día generar build de test <!-- .element: class="fragment" data-fragment-index="1" -->
* Últimos 10 minutos de jam <!-- .element: class="fragment" data-fragment-index="2" -->
* Item 1 <!-- .element: class="fragment" data-fragment-index="3" -->

<div class="fragment"  data-fragment-index="4" style="display:inline-block; text-align:right;">
things here are all

right aligned

blabla


---

# titulo

<div class="container">

<div class="col">

```python
print("Is the rendering bad?")
print("Yeah!")
print("How can you be sure?")
print("Look at the beak of Tux")
```
<!-- .element: style="width: 100%;" -->

</div>

<div class="col">

![tux](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2b/Tux-simple.svg/768px-Tux-simple.svg.png)

</div>

---

# tabla

<table>
  <thead>
    <tr>
      <th>variable</th>
      <th>class</th>
      <th>description</th>
    </tr>
  </thead>
  <tbody>
    <tr class="fragment" data-fragment-index="1">
      <td>character_1_gender</td>
      <td>character</td>
      <td>The gender of the older character</td>
    </tr>
    <tr class="fragment" data-fragment-index="2">
      <td>character_2_gender</td>
      <td>character</td>
      <td>The gender of the younger character</td>
    </tr>
  </tbody>
</table>
---

# CI (Integración Continua)

* Es la traca matraca
* Build y publicar con cada cambio
* Automático
* Es código: no miente ni se olvida pasos

<span style="font-size: 30px;">Recurso para Github y Gitlab: https://github.com/abarichello/godot-ci</span>

---

# Github Actions

* Porque Microsoft lo da gratis, pero hay otros
* workflow.yml: fichero de configuración
    * Define los pasos para hacer build
    * En forma de comandos de terminal

---

# workflow.yml

* Descarga proyecto e img Docker
* Descarga datos + caché
* Versionado
* Setup export templates
* Build
* Deploy
* Notificación en discord 👍/👎 

<img 
    style="width: 20%; position: fixed; top:40%; right: 0%;" 
    src="https://s3.amazonaws.com/static.slid.es/logo/v2/slides-symbol-512x512.png" 
    />

--

![Sample image](https://s3.amazonaws.com/static.slid.es/logo/v2/slides-symbol-512x512.png)

---

# Ejemplo

* Github Actions
* Selecciona workflow
* Lanzar (hacer rama para <br/>q se vea q pasa cuando falla / <br/>hacer como sorpresa)

<img 
style="width: 20%; position: fixed; top:20%; right: 0%;" 
src="https://s3.amazonaws.com/static.slid.es/logo/v2/slides-symbol-512x512.png" 
/> 

```js [1-2|3|4]
let a = 1;
let b = 2;
let c = x => 1 + 2 + x;
c(3);
```

---

### Nuestra experiencia: problemillas

* Queremos usar FMOD en el proyecto
    * Descargar la librería
    * Importarla en el motor

---

### Problema 1: descargar la librería

* Muy pesada (300MB)
    * No podemos subirla a git directamente
    * No podemos descargarla cada vez
* Lo ideal sería usar LFS
    * Límite en proyectos gratuitos (1GB/mes)
* Aún queda descargar los banks

---

### Problema 1: descargar la librería

* ¿Solución? -> Cachear ✅
* ¿Miss de caché?
    * Descarga
    * Guarda en caché

---

### Problema 2: importar librería FMOD

* Godot tiene que importar la librería
* Bug: no espera a terminar de importar antes de empezar la build del proyecto

---

### Problema 2: importar librería FMOD

* Forzar una espera con un hack
    * Esperar a que el procesador esté pausado
    * Mater el proceso para volver a lanzarlo
* [Issue 1362](https://github.com/godotengine/godot-proposals/issues/1362) (¡abierta desde 2020!)
* Aún estamos esperando a Godot
    * La próxima versión siempre es la buena

---

### ¿Conclusiones?

![./images/juez](./images/juez.jpg)

---

### ¡Debate!

* ¿Os mola el tema? ¿Os pica aprender de CI?
* ¿Cómo descargaríais la librería vosotres?
* ¿Os apuntáis a darle 👍 a la issue para que la resuelvan antes? 👀

---

# Enlaces

* Pipeline de desarrollo con Godot 4: https://www.youtube.com/watch?v=ZclZTdIf_K0
* https://github.com/abarichello/godot-ci
* https://blog.jnepo.dev/posts/ci-config-para-jams.html
