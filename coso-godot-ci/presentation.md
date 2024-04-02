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

# CI (Integración Continua)

* Es la traca matraca
* Build y publicar con cada cambio
* Automático
* Es código: no miente ni se olvida pasos
```

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